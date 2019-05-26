Today I gonna tell you about regular expressions. This topic was very captivating for me. I hope you will also enjoy it. So let’s get started. 
**slide**
The first thing that I want you to understand is what regular expression is.
A regular expression is a pattern that is matched against a subject string from left to right.
Pretty complicated, isn’t it? Let’s make it more simple.

Every character and every word that we have in our world is a regular expression. Also it is a search pattern which allows us to use it while we are working with text.
**slide**
Here you can see a regular expression which is used to look for usernames. Looks horrifying, but I promise it will become more clear for you during my presentation. All we need to understand here that it works. That we have the regular expression and we have the result that we were looking for. I gonna teach you something that is useful. All people like useful things.
**slide**
As I said earlier every sign and every word is a regular expression. So we will take as example word “hello” and if we want to match this word in our text, we need to remember that every character matters. As a regular expression this world would be read literally as Upper case H followed by lowercase e followed by lowercase l followed by lowercase l followed by lower case o.
**slide**
Different programming languages ​​use regular expressions a little differently, in this presentation we will consider the most basic examples that will work well in javascript.
**slide**
To create a searching pattern, we need to describe to computer what are we looking for. Now I will show you how different groups of characters can be described in regular expressions.
Back slash lower case d will look for digits.
Back slash lower case w will match either any letter from A to Z (both upper and lower case) or a digit.
Back slash lower case s matches any whitespace.
Dot describes any character. And back slash dot is looking for literal dot
Back slash upper case W means something which is nether any latter in upper or lower case, no a digit.
Back slash upper case S looks for  not a whitespace.
**slide**
For example:
Here we can see a searching pattern consisting of 4 characters following one by one. Each of this signs might be any letter from A to Z (both upper and lower case) or a digit. The result is presented in a lower part of slide. 
**slide**
In our second example we have changed the description of the second character. Now it might be any digit. The pattern was changed and as you see the result is different.
**slide**
The last example shows the regular expression which matches white spaces or double white spaces. It might be useful to correct all double spaces that we accidently put in our text.
**slide** 
All this examples were matching every described character separately. More often we are looking for words that are a sequence of characters and might have different length. It means that it is a time to talk about quantifies. 
**slide**
And in this case star will describe a length of zero or more characters, plus of one or more, question mark of zero or one. By using curved brackets we can set the range of minimum and maximum length or set the exact amount of characters. 
**slide**

 Examples:
This regular expression is looking for sequence of characters which is 5 signs long/ And each od this characters might be either any letter from A to Z (both upper and lower case) or a digit.
**slide**
And now, to make it even more useful…  American English and British English has noticeable difference in spelling of this words.  So if we want to find this words in our text (which is not marked as American or British one) we have to improve our regular expression the way it is shown here.
**slide**
In this case question marc refers that previous latter might be or might not be in the word. 
**slide**
One more opportunity to consider is a description of word position in a text.  By using caret we describe the first word in the line, by using dollar – the last one. Slash be gives us opportunities to set word boundaries. 
**slide**
Let’s go through some examples.
The first regular expression matches character sequence consisting of either latters in upper or lower case or digitals which might have any length. Here we can see examples of using caret and dollar signs. And finally the result of using both of them at the same moment (the meaning in this case is one word line).
**slide** 
And now, using slash b we can finally match the word with exact number of characters.
Now I want to say few words about character classes and alternation. As you can see on the slide square brackets are referring to character classes and round brackets with vertical bar - to alternation.
**slide**
The information that is written in the brackets represents that we are looking just for one option of all that were written.

We use square brackets if we are looking for one symbol. And we use round brackets and vertical bars if it something more than that.
**slide**
Here you can see what looks like a searching pattern for any email.
**slide**
It’s important to know that dot or star, or any another Meta Charapter after putting inside of square brackets turns to literal Characters.  Hyphen inside of square brackets also turns to literal Character but if you see something like [a-z] it will mean the whole range of latters in lower case. Caret in the square brackets means NOT.
**slide**
Another way to use round brackets in regular expressions is to set caption groups. It will give us possibility to work with text more effectively for example to change or replace some part of our match.
**slide**
The most useful example in this case is the one with private telephone numbers.
**slide**
With this regular expression we have divided telephone number on several parts. Starting with plus and following by code of the country and operators code. The body of the number we also divided into two parts. Next step is to set caption groups one and two. It helps us to hide some private information by using tools/ the most important is that all numbers in the texts will be corrected.
**slide**
One interesting example how we can correct links in MD (markdown) format to HTML by using regular expressions . We make it almost in the same way by setting caption groups and using tools to correct them. And here it is.
**slide**

Lastly, remember that you can refer to this any of caption groups inside of regular expression, by writing  back slash plus and number of group , if you want to find exactly the same match.
 For example this regular expression matches all cases when two same words stay in the text together.  
The end
