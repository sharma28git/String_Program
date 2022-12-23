# Globalgit

A sentence is a list of words that are separated by a single space with no leading or trailing spaces.

You are given an array of strings sentences, where each sentences[i] represents a single sentence.

Return the maximum number of words that appear in a single sentence.

Input: sentences = ["alice and bob love leetcode", "i think so too", "this is great thanks very much"]

Output: 6

#Program

public class MyClass {
    
    static int mostWordsFound(String[] sentences){
        int max = 0;
        for(String sent :sentences)
            max = Math.max(max,sent.split(" ").length);
        return max;
    }
    // static int mostWordsLength(String[] str)
    // {
    //     int max = Integer.MIN_VALUE;
    //     int count = 0;
    //     for(int i=0;i<str.length;i++){
    //         String st = str[i];
    //         for(int j=0;j<str.length;j++){
    //             if(str.charAt(j) == ' '){
    //                 count++;
    //             }
    //             if(j == str.length()-1){
    //                 count++;
    //             }
    //         }
    //         if(count > max){
    //             max=count;
    //         }
    //         count=0;
            
    //     }
    //     return max;
    // }
    public static void main(String args[]) {
        String str [] ={"alice and bob love leetcode", "i think so too", "this is great thanks very much"};
        System.out.print(mostWordsFound(str));
    }
}

Q. 2
Count occurrences of a word in string

#Program

public class MyClass {
    static int countOccuerence(String str, String word)
    {
        String [] a = str.split(" ");
        
        int count=0;
        for(int i=0;i<a.length;i++){
            if(word.equals(a[i])){
                count++;
            }
        }
        return count;
    }
    public static void main(String args[]) {
      String str = "Geeks for geeks A computer science portal for geeks ";
      String word = "geeks";
      System.out.print(countOccuerence(str,word));
    }
}

Q. 3 
Check if a string is substring of another
Input: S1 = “for”, S2= “geeksforgeeks”
Output: 5
Explanation: String “for” is present as a substring of s2.

#Program:
public class MyClass {
    static boolean checkSubString(String s1, String s2)
    {
        int M = s1.length();
        int N = s2.length();
        
        for(int i=0;i<=N-M;i++){
            int j;
            for(j=0;j<M;j++){
                if(s2.charAt(i+j) != s1.charAt(j)){
                    break;
                }
            }
            if(j == M){
                return true;
            }
        }
        return false;
    }
    public static void main(String args[]) {
        String s1 = "geeks";
        String s2 = "Geeks for geeks A computer science portal for geeks ";
        boolean A = checkSubString(s1,s2);
        System.out.print(A+" ");
    }
}
