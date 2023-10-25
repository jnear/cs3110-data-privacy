---
title: CS 3110/5110 Data Privacy
layout: default
---

# UVM CS 3110/5110: Data Privacy (Fall 2023)

  * [Course Description](#course-description)
  * [Administrative](#administrative)
  * [Resources](#resources)
  * [Textbook & Other References](#textbook---other-references)
  * [Policies](#policies)
    + [Grading](#grading)
    + [Exams & Quizzes](#exams---quizzes)
    + [Homework Assignments and In-class Exercises](#homework-assignments-and-in-class-exercises)
    + [Late Work](#late-work)
    + [Collaboration & Allowed References](#collaboration--allowed-references)
  * [Final Projects](#final-projects)
  * [CS Student Research Day & Extra Credit](#cs-student-research-day--extra-credit)
  * [Schedule](#schedule)

## Course Description

How can we learn from sensitive data collected from individuals, while protecting the privacy of those individuals? 

This question is central to the study of data privacy,
and is increasingly relevant with the widespread collection of our personal data.
Analysis of this data can lead to important benefits for society,
including advances in medicine and public infrastructure,
but can also result in privacy breaches that expose our most closely-held secrets.

This course will explore both threats to privacy and solutions to the data privacy problem.
We will demonstrate that traditional approaches to protecting privacy, such as anonymization,
are subject to powerful attacks that reveal individuals' sensitive data.
We will see that while more recent approaches for protecting privacy, including k-anonymity and l-diversity,
are more resistant to these attacks, they are not immune.

Then, we will explore recent formal notions of privacy, including differential privacy.
Differential privacy provides a rigorous formal definition of individual privacy that enables a wide range of
statistical analyses while protecting privacy.
We will explore a number of differentially private algorithms for analytics and machine learning,
and learn about the algorithmic building blocks and proof techniques used to develop them.

In addition to learning about the mathematical foundations of differential privacy,
we will explore its practical implications.
We will learn about existing practical systems for enforcing differential privacy and examine the challenges of building such systems.
This course will include programming assignments and an end-of-semester project,
in which students are expected to demonstrate both mastery of the concepts we explore and understanding of
their practical implications by building their own systems that perform privacy-preserving analyses on real data.

## Learning Objectives

By the end of this course, you will be able to:

- Describe the problem and challenges of data privacy
- Conduct a privacy attack on de-identified data
- Define and apply formal notions of privacy, including k-Anonymity and differential privacy
- Design differentially private algorithms and argue that they are correct
- Evaluate the accuracy and efficiency properties of differentially private algorithms

## Administrative

- **Lecture**: Monday, Wednesday, Friday, 1:10pm - 2:00pm, at Dewey Hall 314
- **Instructor**: Joe Near (jnear at uvm dot edu)
- **Graduate Teaching Assistant**: Nikhilsai Reddy Choppa
- **Office hours**: 
  - **Joe Near** (instructor): Mondays and Fridays, 9:30am-10:30am, and by appointment; Innovation Hall E458 (or MS Teams)

## Resources

- **Course textbook** is available [online](https://programming-dp.com) or as a [PDF](https://github.com/uvm-plaid/programming-dp/blob/master/book.pdf)
- **Brightspace** for the course:
  - [CS 3110 (undergrad section)](https://brightspace.uvm.edu/d2l/home/31545)
  - [CS 5110 (graduate section)](https://brightspace.uvm.edu/d2l/home/31615)
- **Course Github Repo** [is available here](https://github.com/jnear/cs3110-data-privacy)
- **Weekly exercises**
  - [Download exercises here](https://github.com/jnear/cs3110-data-privacy/tree/master/exercises)
  - Turn in notebook files on Brightspace
- **Homework assignments** 
  - [Download notebooks here](https://github.com/jnear/cs3110-data-privacy/tree/master/homework)
  - Turn in notebook files on Brightspace
- **Discussions** will take place on MS Teams
- **Slides** from lecture are available [here](https://github.com/jnear/cs3110-data-privacy/tree/master/slides)
- **Review Sheets** for exams:
  - [Exam 1](https://github.com/jnear/cs3110-data-privacy/blob/master/slides/exam1-review.md)
  - [Exam 2](https://github.com/jnear/cs3110-data-privacy/blob/master/slides/exam2-review.md)

## Textbook & Other References

Please **do not** buy any books for this course. All required reference material is available online for free.

The primary textbook we will use for this course is:

- [Programming Differential Privacy](https://programming-dp.com)  
  Joseph P. Near and Chiké Abuah.  
  Also available as a [PDF](https://github.com/uvm-plaid/programming-dp/blob/master/book.pdf)

The following resources may also be useful for additional reading:

- [D&R] [The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/Papers/privacybook.pdf)  
  Cynthia Dwork and Aaron Roth.
  
- [Nissim] [Differential Privacy: A Primer for a Non-technical Audience](https://privacytools.seas.harvard.edu/files/privacytools/files/pedagogical-document-dp_new.pdf)  
   Kobbi Nissim, Thomas Steinke, Alexandra Wood, Micah Altman, Aaron Bembenek, Mark Bun, Marco Gaboardi, David R. O’Brien, and Salil Vadhan.

In addition to these, we will reference a number of academic papers throughout the semester (especially for the section on privacy-preserving machine learning).

### Links and Helpful Resources

 - [How to set up Jupyter Notebooks](https://jnear.github.io/cs3110-data-privacy/jupyter)
 - [Definitions and formulas](https://github.com/jnear/cs3110-data-privacy/blob/master/slides/formulas.pdf) that may be helpful on quizzes and exams
 - [Notes on probability distributions](https://www3.nd.edu/~rwilliam/stats1/x11.pdf)
 - [Intro to differentially private machine learning](https://github.com/jnear/cs3110-data-privacy/blob/master/slides/Intro%20to%20machine%20learning.ipynb)
 - [Variants of differential privacy](https://github.com/jnear/cs3110-data-privacy/blob/master/slides/privacy_definitions.pdf)

## Policies

### Grading

Your grade for the course will be determined as follows:

- 10 homework assignments (5% each; 50% total)
- in-class weekly exercises (20% total)
- midterm exam (10%)
- final exam (10%)
- final project (10%)

Your final grade will be determined by summing the total number of
points awarded and calculating the percentage of the total possible
points. This percentage is translated into a letter grade as follows:

#### Undergraduate Students

| Percent | Letter Grade |
| ------: | ------------ |
| 98-100  | A+           |
| 93-97   | A            |
| 90-92   | A-           |
| 87-89   | B+           |
| 83-86   | B            |
| 80-82   | B-           |
| 77-79   | C+           |
| 73-76   | C            |
| 70-72   | C-           |
| 67-69   | D+           |
| 63-66   | D            |
| 60-62   | D-           |
| <60     | F            |

#### Graduate Students

| Percent | Letter Grade |
| ------: | ------------ |
| 98-100  | A+           |
| 93-97   | A            |
| 90-92   | A-           |
| 87-89   | B+           |
| 83-86   | B            |
| 80-82   | B-           |
| 77-79   | C+           |
| 73-76   | C            |
| 70-72   | C-           |
| <70     | F            |

### Exams & Quizzes

There will be two exams: a midterm and a final. You will be allowed unlimited notes for each exam (but please don't print a whole book). See the schedule below for the dates.

### Homework Assignments and In-class Exercises

This course will use Python for examples and for programming
assignments.  Students are expected to be proficient in Python
programming.  Programming assignments will be distributed and turned
in as Jupyter notebooks. [Click
here](https://jnear.github.io/cs3110-data-privacy/jupyter) for
instructions on installing Jupyter Notebook.

**Assignment Submission**: Homework and in-class exercises will be
turned in via Brightspace.

To submit an assignment:

1. Complete the released Jupyter Notebook by filling in answers to all the questions
2. Submit the notebook file (the .ipynb file) as your solution on Brightspace

*Please* do not change the name of the .ipynb file. This makes the
grading process more difficult.

Please let me know if you have any questions about the submission process.

**Grading rubric**:

100% - Correct or with minor issues
 - Code: runs without error, appears correct or with only minor issues
 - Written: coherent and correct, perhaps with minor details missing

75% - Main idea on the right path, with parts incorrect
 - Code: appears complete and appears to implement the right idea;
   code may throw errors and give incorrect results
 - Written: gets the main idea mostly correct; addresses all or nearly
   all of the required points; may contain some conceptual errors

50% - Decent start, but misses the main idea
 - Code: appears to attempt to implement an approximation of the right
   idea; code may be incomplete and not run at all
 - Written: attempts to approximate the main idea; may avoid
   addressing many required points; may contain major conceptual
   errors

0% - Missing/no answer

**Solutions and feedback**: Homework solutions will be posted on
Brightspace under "homework solutions." Grades will be posted on
Brightspace. To see your graded assignment, visit the following link:

```
https://jnear.w3.uvm.edu/cs3110_feedback/<your-netid-here>
```

Replace `<your-netid-here>` with your actual netid. You will need to
log in using your UVM credentials to view your graded assignments. If
you have questions about how a question was graded, or if you spot a
mistake in grading, please let me know.


### Late Work

Late work *may* be accepted, but you *must* make arrangements with me
first. If you need to turn something in late, for any reason, please
email me *before the deadline*. Depending on the circumstances, I may
(or may not) impose a late penalty on your grade.

### Collaboration & Allowed References

Collaboration on the high-level ideas and approach on assignments is encouraged.
Copying someone else's work is not allowed.
Any collaboration, even at a high level, must be declared when you submit your assignment, in a note at the top of the assignment.
E.g., "I discussed high-level strategies for solving problem 2 and 5 with Alex."

The official references for the course are listed in the schedule below.
Copying from references other than these is not allowed.
In particular, code and proofs should not be copied from other sources,
including Stack Overflow and other public sources.

Students caught copying work are eligible for immediate failure of the course and disciplinary action by the University.
All academic integrity misconduct will be treated according to [UVM's Code of Academic Integrity](https://www.uvm.edu/policies/student/acadintegrity.pdf).

## Final Projects

The course will include a final project, completed in groups of 1-3 students.
The final project will demonstrate your mastery of the concepts covered in this course
by implementing a practical system to perform privacy-preserving analysis of realistic data.

Click [here](https://jnear.github.io/cs3110-data-privacy/projects) for more complete information.

## CS Student Research Day & Extra Credit

We will **not hold class** on **Friday, September 15**. I encourage you
to attend [CS Student Research
Day](https://go.uvm.edu/6v091) and learn about
the awesome research being done by CS students at UVM!

- If you attend **one full session** of talks (or 4 talks total), **take
  brief notes on the talks you hear**, and **send the notes to me via
  email by 11:59pm on September 16**, I will give **1% extra credit to
  your final grade in the course**

## Schedule

Note that class will **not** be held on the following dates:

- Monday, September 4 (Labor Day)
- Friday, September 15 (please attend [CS Student Research Day](https://go.uvm.edu/6v091)
- Friday, October 13 (Fall Recess)
- November 20-24 (Thanksgiving)

Note that class will be **asynchronous** on the following dates:

- Wednesday, September 27
- Friday, September 29
- Friday, October 27
- Monday, October 30

Important due dates:

- Homework assignments are due every *Monday* at 11:59pm.
- In-class weekly exercises are due every *Friday*, by 11:59pm.

Exam dates:

- Midterm exam: Wednesday, October 11, during class (Dewey 314)
- Final exam: December 11, 1:30pm - 2:30pm (Dewey 314)

Homework dates:

|                                                                                            Item | Due Date |
|------------------------------------------------------------------------------------------------:|----------|
| [Homework 1](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_1.ipynb) | 9/11/23  |
| [Homework 2](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_2.ipynb) | 9/18/23  |
| [Homework 3](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_3.ipynb) | 9/25/23  |
| [Homework 4](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_4.ipynb) | 10/2/23  |
| [Homework 5](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_5.ipynb) | 10/16/23 |
| [Homework 6](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_6.ipynb) | 10/23/23 |
| [Homework 7](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_7.ipynb) | 11/1/23 |
| [Homework 8](https://github.com/jnear/cs3110-data-privacy/blob/main/homework/CS3110_HW_8.ipynb) | 11/6/23  |
|                                                                                      Homework 9 | 11/13/23 |
|                                                                                     Homework 10 | 12/4/23  |
|                                                                               Project proposals | 11/17/23 |
|                                                      Final project writeup/video/implementation | 12/11/23 |

Schedule of topics:

| Week of... | Topics                                                                               | Reference |
| ---------: | ------------------------------------------------------------------------------------ | --------- |
| 8/28/23    | Intro to data privacy; de-identification; re-identification (no exercise)            | Ch. 1     |
| 9/4/23     | k-Anonymity and l-Diversity (no class Monday)                                        | Ch. 2     |
| 9/11/23    | Intro to differential privacy; Laplace mechanism (no class Friday)                   | Ch. 3     |
| 9/18/23    | Sensitivity; post-processing; composition & privacy budget; unit of privacy          | Ch. 4, 5  |
| 9/25/23    | Clipping; approximate DP; Advanced composition; Gaussian mechanism                   | Ch. 6     |
| 10/2/23    | Local sensitivity; propose-test-release, smooth sensitivity, sample-and-aggregate    | Ch. 7     |
| 10/9/23    | *Intermission.* Review (exam Wednesday; no class Friday; no exercise)                | None      |
| 10/16/23   | Recent variants of differential privacy                                              | Ch. 8     |
| 10/23/23   | Exponential mechanism; sparse vector technique                                       | Ch. 9, 10 |
| 10/30/23   | Privacy-preserving machine learning; differentially private SGD                      | Ch. 12    |
| 11/6/23    | Local differential privacy                                                           | Ch. 13    |
| 11/13/23   | Differentially private synthetic data                                                | Ch. 14    |
| 11/20/23   | No class (Thanksgiving)                                                              |           |
| 11/27/23   | Privacy in deep learning; Practical systems for privacy                              |           |
| 12/4/23    | Open challenges; review                                                              |           |

# Accommodations

In keeping with University policy, any student with a documented
disability interested in utilizing accommodations should contact SAS,
the office of Disability Services on campus. SAS works with students
and faculty in an interactive process to explore reasonable and
appropriate accommodations, which are communicated to faculty in an
accommodation letter. All students are strongly encouraged to meet
with their faculty to discuss the accommodations they plan to use in
each course. A student's accommodation letter lists those
accommodations that will not be implemented until the student meets
with their faculty to create a plan. Contact SAS: A170 Living/Learning
Center; 802-656-7753; access@uvm.edu; or www.uvm.edu/access

# Religious Holidays

Students have the right to practice the religion of their choice. Each
semester students should submit in writing to their instructors by the
end of the second full week of classes their documented religious
holiday schedule for the semester. An arrangement can then be made to
make up the missed work.

# Student Athletes

In order to be excused from classes, student athletes should submit
appropriate documentation to the Professor in advance of all
scheduling conflicts within the first two weeks of class. Those
missing class are expected to submit make-up assignments within a
reasonable time period.
