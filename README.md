Download Link: https://assignmentchef.com/product/solved-cisc5300-project0-learn-to-use-an-editor
<br>
Project # 0

<ol>

 <li>Learn to use an editor. It is suggested that you learn emacs. Although other editors (such as pico and gedit) may be simpler to learn, emacs provides numerous features that make a programmer’s life easier.</li>

</ol>

You can learn emacs by going through the built-in tutorial.

(a) If you’re using the X-windows (graphical) interface, you can fire up emacs in one of two ways:<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>

<ul>

 <li>You can launch a Terminal window. Having done so, you now enter the command “emacs &amp;” into a terminal window. (Note the ampersand!)</li>

 <li>You can launch Emacs directly from the graphical interface.</li>

</ul>

Once you’ve launched emacs, you can find its tutorial the Help menu in the emacs menu bar.

(b) If you’re using a text-based interface, you should enter the command “emacs” into your terminal window. (Unlike the previous case, there is <em>no </em>ampersand here!) Within emacs, you should type “C-_ t” (that’s control-underscore, followed by a“ t”; no space should appear between them). This is not “C-_ C-t”; that is, don’t hold the control button down when you type the “t”!

<ol start="2">

 <li>Create a directory that will be dedicated to your work on this project. The shell command<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a></li>

</ol>

mkdir -p ˜/private/programming-c++/proj0

will do this. (This will be explained further in class.) Make sure that any work you do is restricted to this directory. One way to ensure this is by issuing the shell command

cd˜/private/programming-c++/proj0

before doing any work on this project. (For instance, you would do this before running emacs.)

<ol start="3">

 <li>Write and run a program that prints “Hello, world!”. The text of such a program is found on the last page of this document. You are to create this program in a computer file proj0.cc, compile it, and run it.</li>

</ol>

It should go without saying that you are to use your name, rather than mine, along with the proper date!

(a) Your first step in creating such a program is to put yourself in the working directory that you created in step 2 above, and then fire up emacs, telling it to edit the file proj0.cc. In other words, you’ll fire up a

Terminal window, and issue the commands

cd ˜/private/programming-c++/proj0 emacs proj0.cc &amp;

inside said window.

<ul>

 <li>After you’ve written (and saved) a correct version of proj0.cc, you can compile it from within emacs. Assuming that you’ve followed directions so far, you should be within the proj0.cc buffer, which should be in C++-mode (look at the modeline at the bottom of the emacs buffer). Give the command “C-c C-c”, which should bring up the prompt “Compile command:” in the minibuffer (underneath the modeline), as well as its expected default response (which is “make -k”). Delete the “make -k”, replacing it with</li>

</ul>

g++ -o proj0-std=c++17proj0.cc

If there are any compilation errors, you can go to the offending line by using “C-c C-e”; you can then fix the error and recompile as before.

<ul>

 <li>To test your program, go over to the Terminal window you created in step 3(a) above, and type the command</li>

</ul>

proj0

It should produce the output

Hello, world!

on a line by itself.

<ul>

 <li>Once your program is running correctly, use the photo program so you can have something to turn in.</li>

</ul>

This command is run within a Terminal window; make sure that ˜/private/programming-c++/proj0 is the working directory.

<em>Do not do this until the program is finished!!!</em>

The commands you should issue are as follows:

photo cat proj0.cc g++ -o proj0-std=c++17proj0.cc proj0 exit

This will create a file, named typescript, in the current directory, containing a listing of proj0.cc, and a sample execution. You should “clean” the typescript by running the command

photo-clean &lt; typescript &gt; proj0.out

(The first “&lt;” is optional.)

(e) You can submit a program in one of several ways.

<ul>

 <li>You can print it out on the printer in the lab. You should <em>not </em>do this unless you are working in the lab! If proj0.out is short (one page), use the command</li>

</ul>

lprproj0.out

If lpr complains, you should use

enscript proj0.out

If proj0.out is longer than one page, use the command

enscript -2r proj0.out

<ul>

 <li>If you’re working at home, you can transfer the proj0.out back to your home computer, and then print it out locally. How this is done will depend on what computer you have at home.</li>

 <li>You can mail it to me, using the command</li>

</ul>

mail -s “Project 0” agw &lt; proj0.out

I’ll send you a receipt when I read said email message.

Note: The online help document (found at <a href="http://www.fordham.edu/cishelp">http://www.fordham.edu/cishelp</a><a href="http://www.fordham.edu/cishelp">)</a> gives more details about submitting a programming assignment. In particular, it will steer you around possible problems. <em>Read it!!</em>

The morbidly curious might want to look at <a href="http://www.helloworldcollection.de">http://www.helloworldcollection.de</a><a href="http://www.helloworldcollection.de">,</a> which is a collection of HelloWorld programs in hundreds of different computer languages. It also gives you an idea of the variety of programming languages out there.

2

Here’s the “Hello, world” program. Once again, thesymbol represents a blank.

/**********************************************************************

*

<ul>

 <li>Project 0: My first program in C++</li>

</ul>

*

<ul>

 <li>Author: A. G. Werschulz</li>

 <li>Date: 15 Elul 5778</li>

</ul>

*

<ul>

 <li>This is the canonical first program for C++.</li>

 <li>Its purpose is to show that one knows how to create a program in * one’s particular programming environment.</li>

</ul>

*

**********************************************************************/

#include&lt;bjarne/std_lib_facilities.h&gt;

int main()

cout &lt;&lt; “Hello, world!
”;

3

<a href="#_ftnref1" name="_ftn1">[1]</a> The details of launching these things involve playing around a bit within the graphical interface. I’ll demonstrate this in class.

<a href="#_ftnref2" name="_ftn2">[2]</a> 2Here, the is a blank. Do <em>not </em>put blanks anywhere else in these lines!