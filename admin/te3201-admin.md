<frontmatter>
title: "Admin Info"
footer: footer.md
head: adminHead.md
</frontmatter>

<include src="../common/header.md" />

<div class="website-content" id="main">

# TE3201 Software Engineering

* [Lectures](#lectures)
* [Project](#project)
* [Learning Materials](#learning-materials)
* [Exam](#exam)
* [Grading](#grading)

## Lectures

TUE 1800-2130 in E3‐06‐15

* :worried: No webcast (Reason: the lecture venue does not have the webcast facility)

* The lecture will be broken into small segments (about 30 minutes) of fairly independent parts so that late comers can still follow the remainder of the lecture.

* First 15 minutes will be a recap of previous lecture or free-flow discussion so that those slightly late will not miss the beginning of the lecture proper.

* Python topics will be in the 2nd half of the lecture so that those not interested in learning Python can leave early.

## Learning materials

A customized **online text book** is used for this module. Topic coverage may not follow the exact topic sequence in the book. There are several ways for you to access the text book.
* Full version is [here]({{baseUrl}}/book-adapted/index.html): The relevant sections are embedded under the corresponding week in the [schedule page]({{baseUrl}}/schedule/index.html).
* :scroll: Printable version (excludes exercises) is [here]({{baseUrl}}/book-adapted/print.html). PDF copies of the relevant sections will be uploaded to IVLE, by Monday of each week.  You are encouraged to use the online full version when possible (instead of the printable version or the PDF version), as it has more content %%&nbsp;videos, exercises, etc.%%

<panel header="Helpful info about using the textbook" no-close>
  <include src="../book-adapted/usage.md#body" />
</panel><p/>

[An additional **guide on programming basics**]({{baseUrl}}/programming/index.html) is provided for you to get started or programming. Contents in that guide are to help you do the programming part of the project; they are not examinable in the final exam. Furthermore, we try to use external resources as much as possible in our guide so that you can continue your learning using those resources beyond the scope of this module.

:bar_chart: **Slides** will be uploaded to IVLE _after_ the lecture. Note that lecture slides are to assist in lecture delivery only; they are ==not suitable for printing or as an exam reference==.

## Project

To be done in individually, or teams of 2-3 members.

**Programming language**: The recommended language is Python but another Object-Oriented language (e.g. Java, C#, C++, ...) is acceptable if there is consensus among team members.

### Software to build

You will be building a personal assistant chat-bot software named _PAC_ (_PAC_ is a temporary name; you should give a different name to your own chat bot)

**_Basic_ Functionality**:

1. PAC interface can be text-based (i.e., no need for a graphical UI)
1. PAC helps with storing and retrieving at least **one type of data** that is useful to the user. Some examples of different types of data (you can pick one of them): details of contacts, todo items, appointments, deadlines, reminders, technical terms to remember, etc. Here is an example interaction between a user and a PAC that deals with TODO items:
   ```
   >> Hi, I'm PAC. What can I do to help you with your TODOs?

   add Return library book
   >> TODO added: Return library book

   list
   >> Here are the list of TODOs you have:
   1. Return library book
   2. Do TE3201 exercises
   3. Call back Jina

   delete 2
   >> TODO deleted: Do TE3201 exercises

   are you single?
   >> Sorry. I did not understand your request.

   help
   >> Here are the requests I understand.
   add {TODO description} : adds a TODO to the list
   list : lists all TODOs
   ...

   ```

1. There is **no need for PAC to be able to understand natural language** sentences. It is fine for the user requests to need to follow a strict format. Defining the request format is part of the project. The example interaction given above is just an example only. Hint: try to design a request format that is easy to remember and type.
1. PAC should support **adding, deleting, listing, searching** (by keyword) of data items.
1. _Persistence_: The data should be **stored in the hard disk** so that restarting PAC should not cause a loss of data entered in a previous session.
   1. The data files should be in a human-readable format such as `.csv` (recommended), `xml`, `json`, plain text, etc.


Basic functionality given above counts as 2 _units_ of functionality. On top of that, you are required to add some more _additional functionality_ (of your own choice). The total amount of functionality required is given below.

Team size | Total amount of functionality
--------- | -----------------------
1-person  | 3-4 units
2-persons | 4-5 units
3-persons | 5-6 units

**_Additional_ Functionality**:

Some suggestions for _additional functionality_:
* More attributes for data items e.g., priorities, tags, birthdays
* Multiple data item types e.g., support saving TODOs, appointments, and deadlines
  * Support connections between data items e.g., ability to assign a TODO to a contact
* Multi-user support e.g., assume the software is installed in a common computer in your office and allow multiple users to interact with it
* More ways to query data e.g., find contacts that has a birthday in next 2 days, find all TODOs with high priority, etc.
* Any other feature (get approval from prof before implementing)

### Constraints

1. You should not use relational/SQL databases e.g., MySQL
1. The software should work in a Windows computer that has the latest releases of Java, .NET, and Python 3.
   1. If your software need other software to be installed (e.g., third-party libraries), please get prof's permission first.

### Deliverables

* **Week 8** (mid-term submission): 10%
  * Deadline: Week 8, Tuesday 6pm
  * Functionality: at least most of the basic requirements are fulfilled (you may leave out the _persistence_ requirement)
    * Submission: demo during lecture in week 8.
  * Documentation:
    * Sections to include:
      * Cover page: Include product name, names of team members
      * User stories: Give user stories to cover all current and future functionalities
      * Use cases: Give 2-3 use case descriptions. Choose use cases that require most number of steps or most complicated.
      * Non-functional requirements: Give 5-10 NFRs for the project. Try to include a diverse range of NFRs.
      * Activity Diagrams: Give at least one activity diagram related to the product e.g., an AD that explains a workflow of how the user uses your product or an algorithm in the code. You can use any drawing software (e.g. PowerPoint), or hand-sketch and photograph/scan the diagrams.
    * Submission: upload to IVLE as a `.docx` or `.pdf` file. File name should contain team member names. e.g., `John Doe, Sarah Tan, Viet Ngoc.docx`

* **Week 13** (final submission): 30%
  * Functionality: all functionality
    * Submission:
      * Zip up all source files, upload to IVLE as a single `.zip` file (not `.rar`). File name should contain member names. :alarm_clock: Deadline: week 13 Monday midnight.
      * Demo the product during week 13 lecture. Each person should demo the features s/he implemented. You can use your own computer to demo. Each person will get no more than 5-6 minutes of demo time. Demo schedule to be announced later.
  * Documentation:
    * Include all content included in mid-term submission. ==Refine as per feedback given. Update to match the final product.==
    * Add a **class diagram** to represent the design of your software. If your software is not an OOP solution, draw the diagram to match how you _propose_ to design your software in an OOP approach, if you were to do the project again. [<trigger trigger="click" for="modal:finalSubmission-classDiagram">example</trigger>]
    * Add an **object diagram** to represent the state of your software after the user has entered some data (assuming your software follows the class diagram above). [<trigger trigger="click" for="modal:finalSubmission-objectDiagram">example</trigger>]
    * Give a sample of **test cases** you would use to test the software.
      * <tooltip content="if you are a 2-person team, give 4 test cases">2 x TEAM_SIZE</tooltip> System test cases: Describe what feature is being tested, steps the tester should take, inputs at various steps, and expected outputs. These tests can be manual or automated. [<trigger trigger="click" for="modal:finalSubmission-systemTests">example</trigger>]
      * Unit test cases for <tooltip content="if you are a 2-person team, give test cases for 2 functions">TEAM_SIZE</tooltip> functions/methods in the code: Give inputs and expected outputs. It is not necessary for you to actually implement these tests in code; just describe the purpose of the test case, inputs, and expected output. [<trigger trigger="click" for="modal:finalSubmission-unitTests">example</trigger>]
    * Submission: As before, upload to IVLE in docx or pdf format as a single file. File name should contain member names. :alarm_clock: Deadline: week 13 Monday midnight.

<modal large title="Class diagram example" id="modal:finalSubmission-classDiagram">

Your actual class diagram is ==likely to be simpler== than this example:

<img src="{{baseUrl}}/book/uml/classDiagrams/introduction/what/images/classDiagramExample1.png" width="600" />

</modal>

<modal large title="Object diagram example" id="modal:finalSubmission-objectDiagram">

<img src="{{baseUrl}}/book/oopDesign/associations/basic/images/completeStructure.png" height="120" />

</modal>

<modal large id="modal:finalSubmission-systemTests">

## Sample System Tests

**Test case 1: Launch without prior data**
* Feature being tested : launch of app, without any prior data
* Set up:
  1. Delete all files in the `/data/` folder.
* Steps:
  1. Run the app using the command `python main.py`
  1. Confirm the the app shows a welcome screen and a summary of commands, as shown below:<br>
     {screenshot here}

**Test case 2: Add first contact**
* Feature being tested : adding of a contact when there are no prior data
* Set up:
  1. Launch app without any prior data (similar to `Test case 1` above).
* Steps:
  Input | Expected
  ----- | --------
  Enter command `add` | app shows error message and show the correct format of the `add` command
  Enter command<br> `add John Doe` | app shows list of contacts containing only one person<br> {screenshot here}

</modal>

<modal large id="modal:finalSubmission-unitTests">

## Sample Unit Tests

**Function being tested : `add_contact(current_contacts, new_contact)`**

Description of the function: appends the `Person` object `new_contact` to the `current_contacts` (a list of `Person` objects) if it doesn't contain that person already.

`current_contacts` | `new_contact` | Expected `current_contacts`
---------------- | ----------- | --------
`[]` | `Person('John')` | `[Person('John')]`
`[Person('John')]` | `Person('John')` | `[Person('John')]`
`[Person('John')]` | `Person('Amy')` | `[Person('John'), Person('Amy')]`

</modal>

## Exam

* Total: 2 hours
  * Part 1: MCQ (1 hour)
  * Part 2: Essay (1 hour)
* Open book (any printed or written materials are allowed)

## Grading

* Project: 40%
* Exam: 60%

</div>
