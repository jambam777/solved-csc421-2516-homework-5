Download Link: https://assignmentchef.com/product/solved-csc421-2516-homework-5
<br>
<strong>Submission: </strong>You must submit your solutions as a PDF through MarkUs. You can produce the file however you like (e.g. LaTeX, Microsoft Word, scanner) as long as it is readable.

<strong>Late Submission: </strong>MarkUs will remain open until 3 days after the deadline, after which no late submissions will be accepted. The late penalty is 10% per day, rounded up.

Weekly homeworks are individual work. See the Course Information handout<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> for detailed policies.

Due to the shortened time period, this assignment has only one question, worth 6 points. You get the remaining 4 points for free.

<ol>

 <li><strong>Variational Free Energy [6pts] </strong>Here, your job is to derive some of the formulas relating to the variational free energy (VFE) which we maximize when we train a VAE. Recall that the VFE is defined as:</li>

</ol>

F(<em>q</em>) = E<em>q</em>[log<em>p</em>(<strong>x</strong>|<strong>z</strong>)] − D<sub>KL</sub>(<em>q</em>(<strong>z</strong>)k<em>p</em>(<strong>z</strong>))<em>,</em>

and KL divergence is defined as

D<sub>KL</sub>(<em>q</em>(<strong>z</strong>)k<em>p</em>(<strong>z</strong>)) = E<em>q</em>[log<em>q</em>(<strong>z</strong>) − log<em>p</em>(<strong>z</strong>)]<em>.</em>

We assume the prior <em>p</em>(<strong>z</strong>) is a standard Gaussian:

<em>D                                  D</em>

<em>p</em>(<strong>z</strong>) = N(<strong>z</strong>;<strong>0</strong><em>,</em><strong>I</strong>) = <sup>Y</sup><em>p<sub>i</sub></em>(<em>z<sub>i</sub></em>) = <sup>Y</sup>N(<em>z<sub>i</sub></em>;0<em>,</em>1)<em>.</em>

<em>i</em>=1                              <em>i</em>=1

And the variational approximation <em>q</em>(<strong>z</strong>) is a fully factorized (i.e. diagonal) Gaussian:

<em>D                                  D</em>

<em>q</em>(<strong>z</strong>) = N(<strong>z</strong>;<em>µ,</em><strong>Σ</strong>) = <sup>Y</sup><em>q<sub>i</sub></em>(<em>z<sub>i</sub></em>) = <sup>Y</sup>N(<em>z<sub>i</sub></em>;<em>µ<sub>i</sub>,σ<sub>i</sub></em>)<em>.</em>

<em>i</em>=1                              <em>i</em>=1

For reference, here are the formulas for the univariate and multivariate Gaussian distributions:

<ul>

 <li><strong>[1pt] </strong>Show that</li>

</ul>

F(<em>q</em>) = log<em>p</em>(<strong>x</strong>) − D<sub>KL</sub>(<em>q</em>(<strong>z</strong>)k<em>p</em>(<strong>z</strong>|<strong>x</strong>))<em>.</em>

<em>(Hint: expand out definitions and apply Bayes’ Rule.)</em>

<ul>

 <li><strong>[1pt] </strong>Show that the KL term decomposes as a sum of KL terms for individual dimensions.</li>

</ul>

In particular,

D<sub>KL</sub>(<em>q</em>(<strong>z</strong>)k<em>p</em>(<strong>z</strong>)) = <sup>X</sup>D<sub>KL</sub>(<em>q<sub>i</sub></em>(<em>z<sub>i</sub></em>)k<em>p<sub>i</sub></em>(<em>z<sub>i</sub></em>))<em>.</em>

<em>i</em>

1

CSC421/2516 Winter 2019                                                                                                                            Homework 5

<ul>

 <li><strong>[2pts] </strong>Give an explicit formula for the KL divergence D<sub>KL</sub>(<em>q<sub>i</sub></em>(<em>z<sub>i</sub></em>)k<em>p<sub>i</sub></em>(<em>z<sub>i</sub></em>)). This should be a mathematical expression involving <em>µ<sub>i </sub></em>and <em>σ<sub>i</sub></em>. If you like, you may suppress the <em>i </em>subscripts in your solution.</li>

 <li><strong>[2pts] </strong>One way to do gradient descent on the KL term is to apply the formula from part (c). Another approach is to compute stochastic gradients using the reparameterization trick:</li>

</ul>

∇<em>θ</em>DKL<em>,</em>

where

and

Show how to compute a stochastic estimate of ∇<em><sub>θ</sub></em>D<sub>KL</sub>(<em>q<sub>i</sub></em>(<em>z<sub>i</sub></em>)k<em>p<sub>i</sub></em>(<em>z<sub>i</sub></em>)) by doing backprop on the above equations. You may find it helpful to draw the computation graph. If you like, you may suppress the <em>i </em>subscripts in your solution.

2

<a href="#_ftnref1" name="_ftn1">[1]</a> <a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">http://www.cs.toronto.edu/</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">~</a><a href="http://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/syllabus.pdf">rgrosse/courses/csc421_2019/syllabus.pdf</a>