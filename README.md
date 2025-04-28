# solution-programming-assignment-1---process-synchronization-with-unix-linux-pipes
**TO GET THIS SOLUTION VISIT:** [Solution : Programming Assignment 1 – Process Synchronization with Unix/Linux Pipes](https://www.ankitcodinghub.com/product/solution-programming-assignment-1-process-synchronization-with-unixlinux-pipes/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;143&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Solution : Programming Assignment 1 - Process Synchronization with Unix\/Linux Pipes&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (4 votes)    </div>
    </div>
In this assignment, you will implement a program to synchronize concurrent processes which perform arithmetic operations. This is especially applicable for execution in dual or quad-core computer systems.

You will learn concepts from several computer science disciplines, including compilers, data or architecture, parallel computation, and, of course, operating systems. The input to your program is illustrated by the following example:

main()

{ input_var a,b,c,d;

internal_var p0,p1,p2,p3;

read(a,b,c,d);

cobegin

p0 = a – b;

p1 = c + d;

p2 = a – d;

coend;

p3 = (p0 + p1) * p2;

write(a,b,c,d,p0,p1,p2,p3);

}

The syntax of the concurrent program follows that of C with the following extensions/modications.

input_var

declares input variables to be read by your program using \read”. Each input value is stored in a process you create.

internal_var

declares internal variables whose values will be computed by a process you create. There will be a distinct process to handle the calculation for each internal variable. Statements within a cobegincoend pair can be executed concurrently. Therefore, processes which compute the internal variables in these concurrent statements can be executed concurrently.

In the above example, processes to compute the values of p0, p1, and p2 can be executed concurrently. However, these 3 processes must complete before the process for computing p3 can start. There can be several levels of nesting cobegin-coend pairs and your program should parse these statements correctly. There may be one level of parentheses in one arithmetic operation, and

this also imposes precedence constraints on the processes’ arithmetic operations.

You may want to create an internal precedence graph to store the dependencies among the processes. To synchronize these concurrent processes, you are to use Unix/Linux pipes. For the above example code, there is a pipe (for sending the input value of a) from process a to process p0, and another pipe (for sending the input value of b) from process b to process p0. Process p0

performs the arithmetic operation \a – b” and sends the result via another pipe to process p3 for it to perform the arithmetic operation \(p0 + p1) * p2″.

The output of your program consists of a printout of the values of all input and internal variables

as specied by \write”.

Notes:

To keep the input simple: The variables in read(…) will be in the same order they appear in the input var declaration. There will be no syntax/semantic errors.

There are at most 10 internal variables.

Example for reading input variables:

read(a1,a2,a3,a4) /* values of a1..a4 are stored in an input file or stdin */

The input le contains:

2,4,1,9

or

2 4 1 9

Also, no constants (5 in this example) are allowed in right-hand-side expressions like p1 = a1

+ 5. Only input variables or internal variables are allowed.

Submitting the program:

For submission guidelines, please visit the TAs’ webpage. Also, check the forum there for common questions and answers.

&nbsp;
