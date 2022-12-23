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
