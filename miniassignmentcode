package mini;

/**
 * Utility class with static methods for loop practice.
 */
public class LoopsInfinityAndBeyond {

	/**
	 * Private constructor to disable instantiation.
	 */
	private LoopsInfinityAndBeyond() {
	}

	/**
	 * Define a flying saucer as the following string pattern: one ‘(‘, followed by
	 * zero to many ‘=’, followed by one ‘)’. Write a Java method that, given a
	 * string find the first instance of a flying saucer (starting from the left)
	 * and return its length. If no flying saucer exists return 0.
	 * <p>
	 * For example: Given: "(==)" Return: 4
	 * <p>
	 * Given: "***()**(===)" Return: 2
	 * <p>
	 * Given: "****(***)" Return: 0
	 * 
	 * @param source input string
	 * @return the length
	 */
	public static int flyingSaucerLength(String s) {
		int count = 0;
		int start = -1;
		int i;
		for (i = 0; i < s.length(); i++)
		{
			if (s.charAt(i) == '(')
			{
				count = 1;
				start = i;
				if (s.charAt(i+1)!= '=' && s.charAt(i+1) != ')')
				{
					count = 0;
					break;
				}
			}
			else if (s.charAt(i) == ')')
			{
				if (count > 0)
				{
					return i-start+1;
				}
			}
			else if (s.charAt(i) == '=')
			{
				count++;
			}
			else if (s.charAt(i) != '=')
			{
				continue;
			}
		}
		return count;
	}

	/**
	 * Write a Java method that, given a string which many contain a flying saucer
	 * broken into two parts with characters in between, return a string where the
	 * flying is fixed by removing the in between characters. Look for the two parts
	 * of the flying saucer from left to right and fix the saucer with the first
	 * available parts.
	 * <p>
	 * For example:
	 * Given: ***(==****===)***
	 * Return: ***(=====)***
	 * <p>
	 * Given: ***(==****)**=)*
	 * Return: ***(==)**=)*
	 * <p>
	 * Given: ***(==)**
	 * Return: ***(==)**
	 * 
	 * @param s
	 * @return
	 */
	public static String fixFlyingSaucer(String s) {
	    int openingBracketIndex = -1;
	    int closingBracketIndex = -1;
	    for (int i = 0; i < s.length(); i++) {
	        char c = s.charAt(i);
	        if (c == '(') {
	            openingBracketIndex = i;
	        } else if (c == ')') {
	            closingBracketIndex = i;
	            break;
	        }
	    }
	    if (openingBracketIndex == -1 || closingBracketIndex == -1) {
	        return s;
	    }
	    StringBuilder sb = new StringBuilder(s.substring(0, openingBracketIndex + 1));
	    for (int i = openingBracketIndex + 1; i < closingBracketIndex; i++) {
	        if (s.charAt(i) == '=') {
	            sb.append('=');
	        }
	    }
	    sb.append(s.substring(closingBracketIndex));
	    return sb.toString();
	}

	/**
	 * Write a Java method that, given a string which many contain many flying
	 * saucers, return the number of flying saucers. For this problem a flying
	 * saucer may wrap around from the right side of the string to the left.
	 * <p>
	 * For example:
	 * Given: ***(===)***
	 * Return: 1
	 * <p>
	 * Given: =)**(==)**(
	 * Return: 2
	 * <p>
	 * Given: ***(=*=)**
	 * Return: 0
	 * 
	 * @param s
	 * @return
	 */
	public static int countFlyingSaucers(String s) {
		int count = 0;
		int i;
		for (i = 0; i < s.length(); i++)
		{
			if (s.charAt(i) == '(')
			{
				continue;
			}
			else if (s.charAt(i) == ')')
			{
				count++;
			}
			else if (s.charAt(i) == '=')
			{
				continue;
			}
		}
			return count;
		
	}

	/**
	 * Write a Java method that, given a string which many contain many flying
	 * saucers, shifts all of the saucers one character to the right. For this
	 * problem a flying saucer may wrap around from the right side of the string to
	 * the left. The returned string should have the same number of characters as
	 * the given string. This is achieved by moving the character to the right of a
	 * saucer to its left. It can be assumed that saucers will never be touching
	 * each other (i.e., there will always be at least one character between any two
	 * saucers). Also, a saucer will not touch itself (e.g., "=)(=").
	 * <p>
	 * For example:
	 * Given: ***(===)***
	 * Return: ****(===)**
	 * <p>
	 * Given: =)**(==)**(
	 * Return: (=)***(==)*
	 * <p>
	 * Given: a()bcde(=*=)fg
	 * Return: ab()cde(=*=)fg
	 * 
	 * @param s
	 * @return
	 */
	public static String flyingSaucersFly(String s) {
		String saucers = s;
		String flyingSaucer = "";
		char[] saucer = new char[s.length()];
		char[] newSaucer = new char[s.length()];
		int i;
		for (i = 0; i < s.length(); i++)
		{
			saucer[i] = saucers.charAt(i);
		}
		newSaucer[0] = saucer[saucer.length-1];
		for (i = 1; i < saucer.length; i++)
		{
			newSaucer[i] = saucer[i-1];
		}
		for (i = 0; i < saucer.length; i++)
		{
			flyingSaucer = flyingSaucer + newSaucer[i];
		}
		return flyingSaucer;
	}
}
