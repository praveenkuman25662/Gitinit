# Gitinit
public class PalindromeChecker {
    public static boolean isPalindrome(String str) {
        // Removing all non-alphanumeric characters and converting to lowercase
        String processedStr = str.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        
        int left = 0;
        int right = processedStr.length() - 1;
        
        while (left < right) {
            if (processedStr.charAt(left) != processedStr.charAt(right)) {
                return false; // Characters don't match, not a palindrome
            }
            
            left++;
            right--;
        }
        
        return true; // All characters matched, it's a palindrome
    }
    
    public static void main(String[] args) {
        String str = "A man, a plan, a canal, Panama!";
        
        if (isPalindrome(str)) {
            System.out.println(str + " is a palindrome.");
        } else {
            System.out.println(str + " is not a palindrome.");
        }
    }
}
