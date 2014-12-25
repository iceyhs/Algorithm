{\rtf1\ansi\ansicpg936\cocoartf1265\cocoasubrtf210
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;\f1\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red38\green38\blue38;\red184\green14\blue61;\red247\green238\blue241;
}
\paperw11900\paperh16840\margl1440\margr1440\vieww10380\viewh7200\viewkind0
\deftab720
\pard\pardeftab720

\f0\fs28 \cf2 \expnd0\expndtw0\kerning0
Given a string 
\i \expnd0\expndtw0\kerning0
s
\i0 \expnd0\expndtw0\kerning0
 consists of upper/lower-case alphabets and empty space characters 
\f1\fs26 \cf3 \cb4 \expnd0\expndtw0\kerning0
' '
\f0\fs28 \cf2 \cb1 \expnd0\expndtw0\kerning0
, return the length of last word in the string.\
If the last word does not exist, return 0.\
\pard\pardeftab720

\b \cf2 \expnd0\expndtw0\kerning0
Note:
\b0 \expnd0\expndtw0\kerning0
 A word is defined as a character sequence consists of non-space characters only.\
For example, \
Given 
\i \expnd0\expndtw0\kerning0
s
\i0 \expnd0\expndtw0\kerning0
 = 
\f1\fs26 \cf3 \cb4 \expnd0\expndtw0\kerning0
"Hello World"
\f0\fs28 \cf2 \cb1 \expnd0\expndtw0\kerning0
,\
return 
\f1\fs26 \cf3 \cb4 \expnd0\expndtw0\kerning0
5
\f0\fs28 \cf2 \cb1 \expnd0\expndtw0\kerning0
.\
\
\
public class Solution \{\
    public int lengthOfLastWord(String s) \{\
        if(s.length()==0) return 0;\
        \
        int end;\
        for(end=s.length()-1; end>=0; end--)\{\
            if(s.charAt(end) != ' ') break;\
        \}\
       \
       if(end<0) return 0;\
       \
       int start;\
       \
       for(start=end; start>=0; start--)\{\
           if(s.charAt(start) ==' ') break;\
       \}\
       \
       if (start<0) return end+1;\
       else return end-start;\
       \
       \
        \
    \}\
\}}