# JAVA-ASSIGNMENT
QUESTION 1- package com.Ayush.opps;

public class sum_of_number_string {
    public static void main(String[] args) {
        String str ="1xyz23";
        System.out.println(sum(str));
    }
    static int sum(String str)
    {
        boolean check=false;
        int sum=0;
        int result=0;
        for(char ch : str.toCharArray())
        {
           // char ch=str.charAt(i);
            if(Character.isDigit(ch))
            {
                sum  =sum*10+Character.getNumericValue(ch);
                check =true;
            }
            else {
                if(check)
                {
                    result+=sum;
                    sum=0;
                }
                check=false;
            }
        }
        if(check)
        {result+=sum;}
        return result;
    }
}

QUESTION 2- package com.Ayush.opps;
import java.util.*;
import java.lang.*;
public class anagrams_string {
    public static void main(String[] args) {
        String str="hello";
        String st="olleh";
        System.out.println(check(str,st));
    }
    static boolean check (String str,String st)
    {
        if(str.length() != st.length())
        {
            return false;
        }
        char ch[] =str.toCharArray();
        char c[] =st.toCharArray();
        Arrays.sort(ch);
        Arrays.sort(c);

        str = new String (ch);
        st= new String(c);
        if(str.equals(st))
        {
            return true;
        }
        return false;
    }
}


OUESTION 3- package com.Ayush.opps;
import java.util.*;
public class remove_vowel {
    public static void main(String[] args) {
        System.out.println("enter the string");
     Scanner sc =new Scanner(System.in);
     String str = sc.next();
       String ptr = str.toUpperCase();

        ptr =ptr.replaceAll("[AEIOU]","");
        System.out.println(ptr);
    }

}

QUESTION 4- package com.Ayush.opps;

public class accept_alphabet {
    public static void main(String[] args) {
        String str = "take12% *&u ^$#forward";
        StringBuilder sb= new StringBuilder();

        for(int i=0;i<str.length();i++)
        {
            char ch = str.charAt(i);
            if((ch >=65 && ch<90) || (ch>=97 && ch<=122))
            {
                sb.append(ch);
            }
        }
        System.out.println(sb);
    }
}


QUESTION 5- package com.Ayush.opps;

import java.util.Locale;
import java.util.Scanner;

public class Alphabet {
    static int vowel=0,space=0,consonant=0;
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("enter the string");
        String z =sc.nextLine();
            String str = z.toUpperCase();
        
        for(int i=0;i<str.length();i++)
        {
            char ch=str.charAt(i);
            check(ch);
        }
        System.out.println("vowel ="+vowel +"consonant ="+consonant +"space ="+space);
    }
    public static void check(char ch)
    {
        if(ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U' )
        {
            vowel++;
        }
        else if(ch == ' ')
        {
            space++;
        }
        else{
            consonant++;
        }
    }
}

QUESTION 6- package com.Ayush.opps;
import java.util.*;
public class whitespaces {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String str = sc.next();

        remove(str);
    }
    static void remove(String str)
    {
        String ptr =str.replaceAll(" ","");
        System.out.println(ptr);

    }
}

QUESTION 7- package com.Ayush.opps;
import java.util.*;
public class reverse_string {
    public static void main(String[] args) {
        System.out.println("Enter the String :");
        Scanner sc= new Scanner(System.in);
        String str=sc.nextLine();
        String st="";
        for(int i=str.length()-1;i>=0;i--)
        {
            char ch=str.charAt(i);
            st=st+ch;
        }
        System.out.println(st);
    }
}

OUESTION 8- package com.Ayush.opps;
import java.util.*;
public class pallindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("enter the string");
        String z =sc.nextLine();
        check(z);

    }
    static void check(String str)
    {
        int i=0,j=str.length()-1;
        while(i<j) {


            if(str.charAt(i)!=str.charAt(j))
            {  System.out.println("not pallindrome");
                return;
            }
            i++;
            j--;

        }
        System.out.println("pallindrome");
    }
}


QUESTION 9- package com.Ayush.opps;

public class largest_string {
    public static void main(String[] args)
    {
       String str ="hello worldssss";
        System.out.println(largest(str));
    }
    static String largest(String str)
    {
        String largest="";
        String word[]=str.split(" ");
        for(String s:word)
        {
            if(largest.length()-1<s.length()-1)
            {
                largest=s;
            }
        }
        return largest;
    }
}

QUESTION 10- package com.Ayush.opps;
import java.lang.*;
import java.util.*;
public class capatilize {
    public static void main(String[] args) {
        String str="hello world";
        System.out.println(convert(str));
    }
    static String convert(String str)
    {
        String word[]=str.split(" ");
        StringBuilder sb= new StringBuilder();
        for(String s : word)
        {if(s.length()>1)
        {
            char first=Character.toUpperCase(s.charAt(0));
            char last=Character.toUpperCase(s.charAt(s.length()-1));
            sb.append(first).append(s.substring(1,s.length()-1)).append(last);
        }
        else {
            sb.append(Character.toUpperCase(s.charAt(0)));
        }
        sb.append(" ");

        }
        return sb.toString();
    }
}
