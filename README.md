Download Link: https://assignmentchef.com/product/solved-ece325-lab-1-java-basics-heap-sort-and-eclipse
<br>
Getting familiar with the Eclipse environment, Creating a Java project; creating and editing a Java program, Adding a library to the build path and Running project inside and outside Eclipse

Eclipse

The Eclipse platform is a generic <em>integrated development environment</em> (IDE) foundation without any focus on a specific programming language. The platform contains IDE functionality and is built with components creating applications by using component subsets. Developers create, share and edit generic projects and files in the platform, while participating within a multiple team development environment repository. However, it is written mostly in Java and most of the time is used to develop applications in this programming language, but it covers other languages such as: C, C++, Ruby, R, JavaScript, PHP, Python …

In this lab we will focus on Eclipse usage in writing, editing and running <strong>Java</strong> programs.

<h2>1.2  Java Requirements of Eclipse</h2>

Eclipse requires an installed Java runtime (at least Java 5). Java can be downloaded in two flavors, a JRE

(Java runtime environment) and a JDK (Java development tools) version. The Eclipse IDE contains its own Java compiler hence a JRE is sufficient for most tasks with Eclipse. The JDK version of Java is required if you compile Java source code on the command line and for advanced development scenarios, for example if you use automatic builds or if you develop Java web applications.

<h2>1.3  Eclipse Resources</h2>

<strong>Resource</strong><strong>                                         </strong><strong>URL </strong>

<table width="438">

 <tbody>

  <tr>

   <td width="221">Eclipse Homepage</td>

   <td width="217"><a href="https://www.eclipse.org/">http://www.eclipse.org/</a></td>

  </tr>

  <tr>

   <td width="221">Download Eclipse</td>

   <td width="217"><a href="https://www.eclipse.org/downloads/">http://www.eclipse.org/downloads/</a></td>

  </tr>

  <tr>

   <td width="221">Eclipse Online Tutorials</td>

   <td width="217"><a href="https://www.eclipse.org/resources/">http://www.eclipse.org/resources/</a></td>

  </tr>

 </tbody>

</table>

<h1>2  Deliverable 1 — Create and Run a Simple Java Program (Heap Sort)</h1>

Sort a list of integers using the heap sort algorithm:

<ul>

 <li><a href="https://www.youtube.com/watch?v=WYII2Oau_VY">http://www.youtube.com/watch?v=WYII2Oau_VY</a> (Super short, no words, pictures only)</li>

 <li><a href="https://www.youtube.com/watch?v=B7hVxCmfPtM">http://www.youtube.com/watch?v=B7hVxCmfPtM</a> (The traditional version from M.I.T., very, very long)  Or find your own</li>

</ul>

<strong>Note</strong>: Write carefully, you are going to reuse this code later!

<em>Step 1: Launch Eclipse </em>

<table width="48">

 <tbody>

  <tr>

   <td width="48">eclipse</td>

  </tr>

 </tbody>

</table>

Open the Eclipse IDE. It can be done at terminal by typing .

<em>Step 2: Create a new project </em>

Select <em>File</em> =&gt; <em>New</em> =&gt; <em>Java Project</em> =&gt; Name your project =&gt; <em>Finish</em>.

<em>Step 3: Add a new class </em>

<table width="154">

 <tbody>

  <tr>

   <td width="154"><em>public static void main</em></td>

  </tr>

 </tbody>

</table>

Select your project =&gt; <em>File</em> =&gt; <em>New</em> ⇒ <em>Class</em> =&gt; Name the class =&gt; check <em> </em>

<em>(String[] args)</em> =&gt; <em>Finish</em>.

For this lab, just copy the source file HeapSort.java and paste into the <em>src</em> folder of the project.

<em>Step 4: Implement your class </em>

<table width="669">

 <tbody>

  <tr>

   <td width="68">Finish the</td>

   <td width="28">sort</td>

   <td width="573"> method.</td>

  </tr>

  <tr>

   <td colspan="3" width="669"><em>Step 5: Run you code </em></td>

  </tr>

 </tbody>

</table>

Run the code (<em>Run as</em> =&gt; <em>Java application</em>).

<strong>DEMO this deliverable to the lab instructor. </strong>




<h1>3  Deliverable 2 — Add a Library to the Build Path</h1>

In this part, we want you to edit your source code and add a library to the build path.

<h2>3.1  Edit Your Code</h2>

An <em>import</em> statement is a way of making more of the functionality of Java available to your program. Java can do a lot of things, but you do not need all of them so often. It has its classes divided into <em>packages</em>.

<table width="669">

 <tbody>

  <tr>

   <td width="455">Your own classes are part of packages, too. So, anything that isn’t in the</td>

   <td width="61">java.lang</td>

   <td width="152"> package or the local</td>

  </tr>

  <tr>

   <td colspan="3" width="669">package needs to be imported.</td>

  </tr>

 </tbody>

</table>

<em>Step 1: Import libraries </em>

Add the two following imports to the beginning of your source code:

<strong>import</strong> components.simplewriter.SimpleWriter<strong>;</strong> <strong>import</strong> components.simplewriter.SimpleWriter1L<strong>;</strong>

<em>Step 2: Rewrite the output code </em>

Edit your print/println commands by instantiating an object of SimpleWriter. For example, substitute: System<strong>.</strong>out<strong>.</strong>println<strong>(</strong>array<strong>[</strong>c<strong>]);</strong>

with:

SimpleWriter out <strong>=</strong> <strong>new</strong> SimpleWriter1L<strong>();</strong> out<strong>.</strong>println<strong>(</strong>array<strong>[</strong>c<strong>]);</strong> out<strong>.</strong>close<strong>();</strong>

<em>Step 3: Run your code </em>

Run your code and see there are some errors.

The reason for these errors is that the components in the import lines, SimpleWriter and SimpleWriter1L, are from the components.jar, but we have not told Eclipse to use it yet.

<h2>3.2  Add the Library to Your Project Build Path</h2>

<em>Step 1: Download the library </em>

Save the components.jar in your home directory (or home directory of your project).

<em>Step 2: Configure the project </em>

Right-click on your project =&gt; <em>Build Path</em> =&gt; <em>Configure Build Path</em> =&gt; <em>Add External Jars</em>=&gt; Select the library =&gt; <em>Finish</em>.

Errors should disappear and you would be able to run your code.

<strong>DEMO this deliverable to the lab instructor.</strong>

<h1>4  Deliverable 3 — Run Your Java Code outside of Eclipse</h1>

Eclipse has implemented its own java compiler called <em>Eclipse Compiler for Java</em> (ECJ), which is based on IBM’s Jikes java compiler. Thus, Eclipse is automatically compiling your code on-the-fly to create an instant view of the result. In this part, you need do thing manually.

<h2>4.1  Runable JAR</h2>

A runnable JAR is just like a EXE file in Windows, which means you can double click it to run. However, what your heap sort is doning is just outputting results into the console, so you still need the terminal/cmd/PowerShell to run it.

Select <em>File</em> =&gt; <em>Export…</em> =&gt; <em>Java</em> =&gt; <em>Runnable JAR file</em> ⇒ <em>Next</em>:

<ul>

 <li><em>Launch configuration</em>: select your HeapSort;</li>

 <li><em>Export destination</em>: type your target JAR file path and name;</li>

 <li><em>Library handling</em>: choose the last option <em>Copy required libraries into a sub-folder next to the generated JAR</em>.</li>

</ul>

Click <em>Finish</em>, and you are ready to go:

java −jar HeapSort.jar

<h2>4.2  Compile and Run by JDK</h2>

<em>Step 1: Copy your source codes to home directory </em>

cp src/HeapSort.java ~      <em># “~” refers to the home directory of your account</em> cp components.jar ~

<table width="669">

 <tbody>

  <tr>

   <td width="249">Note: your HeapSort.java must use the</td>

   <td width="81">SimpleWriter</td>

   <td width="34"> and</td>

   <td width="94">SimpleWriter1L</td>

   <td width="211">.</td>

  </tr>

  <tr>

   <td colspan="5" width="669"></td>

  </tr>

 </tbody>

</table>

<table width="61">

 <tbody>

  <tr>

   <td width="61"><em>CLASSPATH</em></td>

  </tr>

 </tbody>

</table>

<em>Step 2: Configure the  </em>

JDK requires an important environmental variable CLASSPATH to compile and run codes. In Linux, you can do it as follows:

export CLASSPATH<strong>=</strong>“your_class_paths”     <em># You need fill in the actual paths</em> echo $CLASSPATH                         <em># Print your class paths</em> In this lab, your have two groups of classes:

<table width="693">

 <tbody>

  <tr>

   <td width="26"></td>

   <td width="278">Your own classes, which in this case is your</td>

   <td width="55">HeapSort</td>

   <td width="335">;</td>

  </tr>

  <tr>

   <td width="26"></td>

   <td colspan="3" width="667">The third party library classes, which is the components.jar.</td>

  </tr>

 </tbody>

</table>

<table width="61">

 <tbody>

  <tr>

   <td width="61">CLASSPATH</td>

  </tr>

 </tbody>

</table>

The  must contain the paths of both groups. Try figure it out.