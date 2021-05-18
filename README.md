# string-palindrom

class aditya
{
    // A recursive function that 
  
    // palindrome or not.
    static boolean isPalRec(String str, 
                            int start, int end)
    {
        
        if (start == end)
            return true;
  
        // If first and last 
        // characters do not match
        if ((str.charAt(start)) != (str.charAt(end)))
            return false;
  
        // If there are more than 
        // two characters, check if
        // middle substring is also
        // palindrome or not.
        if (start < end + 1)
            return isPalRec(str, start + 1, end - 1);
  
        return true;
    }
  
    static boolean isPalindrome(String str)
    {
        int n = str.length();
  
    // An empty string is 
    // considered as palindrome
        if (n == 0)
            return true;
  
        return isPalRec(str, 0, n - 1);
    }
  
   
    public static void main(String args[])
    {
        String str = "geeg";
  
        if (isPalindrome(str))
            System.out.println("Yes");
        else
            System.out.println("No");
    }
}
