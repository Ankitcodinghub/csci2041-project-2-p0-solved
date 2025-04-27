# csci2041-project-2-p0-solved
**TO GET THIS SOLUTION VISIT:** [CSCI2041 Project 2 P0 Solved](https://www.ankitcodinghub.com/product/csci2041-programming-project-2-p0-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124492&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI2041  Project 2 P0 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
CSCI 2041 Advanced Programming Principles

0. Introduction.

In this programming project, you will write an OCaml module whose functions read Lisp thing’s from a file. If we have a function that reads Lisp thing’s, a function that evaluates Lisp thing’s, and a function that prints Lisp thing’s, then we could put them all together to make a complete Lisp system.

1. Theory.

In formal language theory, a language is a set of strings; a string is a sequence of characters. A grammar is a mathematical description of a language that tells which strings are in the set, and which strings are not. One way to specify a grammar is to use mathematical rules, but we won’t do that here. Instead, we’ll use a directed graph called a syntax diagram. A syntax diagram for Lisp thing’s is shown below.

Assignment Project Exam Help

• The box labeled thing stands for a Lisp thing. The diagram is recursive, because it is defined in terms of itself: there is a box labeled thing inside the diagram labeled thing.

• The box labeled number is a Lisp number token. It’s a sequence of one or more digits, ‘0’ through ‘9’, preceded by an optional minus sign ‘−’.

• The box labeled symbol is a Lisp symbol token. It’s a sequence of one or more characters other than blanks, newlines, and parentheses.

• There is no box labeled nil, because it’s simpler to pretend that nil is a symbol, although it really isn’t (see below).

Here are some examples of thing’s that are described by the diagram.

• A number, like 100, is a thing, because we can start on the left, follow arrows to the box labeled number, and then follow arrows out of the diagram again.

• A symbol, like hello, is also a thing, because we can start on the left, follow arrows to the box labeled symbol, and then follow arrows out of the diagram.

• An empty list, like (), is a thing, because we can follow an arrow to the circle labeled ‘(’, follow an arrow to the circle labeled ‘)’, and then follow an arrow out of the diagram. In Lisp, () is another notation for nil (see below).

• A list, like (a b c), is a thing, because we can follow an arrow to the circle labeled ‘(’, and then to the box labeled thing. We imagine that a copy of the diagram thing appears in place of that box. If we follow arrows through that copy, then we find that a is also a thing. If we go around the loop, back to the box labeled thing, we find that b is another thing in the same way, and if we go around the loop again, we find that c is a thing as well. When we exit the loop, we follow an arrow through a circle labeled ‘)’, and then follow yet another arrow out of the diagram.

We could show that nested lists like ((a) b c) and (a (b c)) are thing’s too, by following arrows through the diagram in the same way. And we could show that something like ‘)x(()5(’ is not a thing, because there is no way to follow arrows through the diagram given its characters.

2. Implementation.

Parsers

Assignment Project Exam Help

(5 points.) Signature. This signature must describe the function makeParser and the exception Can’tParse, but nothing else.

Parser

makeParser path

(10 points.) Return a parser: a new function that takes the OCaml unit object () as its only argument. (Do not confuse the OCaml unit object () with the Lisp empty list ()!) Each time it is called, the parser reads the next Lisp thing from the file whose pathname is the string path, and returns that thing.

The function makeParser must make a scanner by calling

Scanner.makeScanner. It must also make a variable called token. The scanner reads tokens from the file whose pathname is path. The variable token holds the token most recently read by the scanner. The scanner and the variable must be visible to the parser returned by makeParser, but invisible to all other functions.

nextThing ()

(10 points.) This function does all the work for the parser returned by makeParser. It examines token and uses it to decide what kind of thing it will read. Then it reads the thing, constructs an OCaml object which represents that thing, and returns the object. It does this in the following way.

If token is CloseParenToken then raise Can’tParse.

If token is EndToken then raise Can’tParse.

If token is NumberToken n then return Number n.

If token is OpenParenToken then read a Lisp list and return it.

If token is SymbolToken “nil” then return Nil (see below).

If token is SymbolToken s then return Symbol s.

Note that nil will be read by the token scanner as a SymbolToken. However, it must be treated as if it is OCaml’s Nil.

nextThings ()

Cons (t1, Cons (t2 …, Cons (tn, Nil) … ))

If nextThings encounters a CloseParenToken, then it must skip that token. If it encounters an EndToken, then it must raise Can’tParse, because this means the Lisp list ended without a CloseParenToken.

Here are some hints about how to write these functions. The scanner and the parser are designed according to similar rules, as follows.

• The scanner reads characters. The parser reads tokens.

• The scanner uses a variable ch to hold the most recently read character from a file. The parser uses a variable token to hold the most recently read token from a file.

• The scanner can tell what kind of token it was about to read by examining the first character of that token (in ch). The parser can tell what kind of thing it is about to read by examining the first token of that thing (in token).

• Whenever a function in the scanner was called, ch always holds the first character of the token to be read. Whenever a function in the parser is called, token always holds the first token of the thing to be read.

• Whenever a function in the scanner returns, ch always holds the next character after the token that was just read. Whenever a function in the parser returns, token always holds the next token after the thing that was just read.

To make some of these rules work, it is necessary to skip tokens after they are read. If nextToken is the name of the scanner created by makeParser, then we can skip a token by writing token := nextToken (). For example, after nextThing reads a SymbolToken, it must skip that token in this way.

3. Examples.

The file things.txt on Canvas contains a series of example Lisp expressions. The file testsP2.ml on Canvas contains a series of calls to a parser created by makeParser. Each call reads the next Lisp expression from things.txt, converts it to an OCaml object, and prints that object.

4. Deliverables.

CHECK to make sure you have submitted the correct file, both Assignment Project Exam HelpBEFORE AND AFTER you turn it in.
