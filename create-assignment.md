# Creating an Assignment

First, sign into [classroom.github.com/classrooms][class-dash]. Choose the classroom that you wish to create the assignment for.
If you have not created a classroom, please read **TODO - Create a Classroom Guide** first.

Click the green _"New Assignment"_ button, which will let you choose between creating an individual assignment, or a group assignment.

## Individual Assignments

![Screenshot of the "New Individual Assignment" page.][screenshot-new-indiv]

On this page, you can configure the parameters for the new assignment.
By default GitHub uses some settings which may be a poor fit for graded
assignments, so these should be changed.

### Repository Privacy 

By default, GitHub will try to use Public repositories for student
assignments. 
[As part of the GitHub Student Developer Pack,][student-pack]
all students with a `.edu` e-mail address should have free use
of GitHub private repos, at no cost to them.

Historically, some students have had trouble redeeming this benefit, and have had
to contact GitHub support. If this is a required step for students to submit their assignments,
it may be best to allow leniency if they are stuck.

TODO edit the previous section

If you have a repo with unlimited private repositories, then your students can freely
use private repositories that under your control, without having to verify as a student first.

### Admin Access

It may be unwise to give students Admin permissions in their repository.
Some features, like force-pushing allow students to amend commits and potentially spoof
the timestamps of when code was committed.

In addition, the student's local time may affect things. TODO might appear that they are committing
from the future. github does not stop them from doing so

### Starter Code

By providing a starter repository (which is optional), all student repos will start with a set of 
files in their repository. This may be useful for distributing instructions or sample files.

Note that all students will have access to the history contained in this repo, including access
to the changes that have been made to the sample repo. Do not keep a solution to the assignment
in the same repository.

### Deadline

You can set a deadline of when code is due. Note that this will not prevent students from making
changes after the deadline, but when viewing project repos from the website, the submission
will count as the last commit pushed before midnight. Note that as of writing, the github classroom
assistant client does not respect these deadlines.

The absolute best way to ensure that students work on assignments past the due date is to
download them as soon as they are due.

TODO - need to see if I can spoof the due date by force pushing or amending dates

### Recommended Settings

These settings are a good starting point when creating a new assignment.

![Screenshot of recommended settings for creating a new assignment.][screenshot-recommended-indiv]

## Managing a New Individual Assignment

After creating a new assignment, you should see a confirmation dialog similar to the following:

![Screenshot of new assignment created confirmation.][screenshot-assignment-confirm]

This page allows you to manage the assignment and view the state of all submissions made
to this assignemnt.

The _"Download Repositories"_ button will open the [GitHub Classroom Assistant software][classroom-assistant]
and open this assignment. This tool enables bulk downloading of all assignments,
and is available for Linux, Windows, and MacOS.

**Important Note:** At the time of writing, GitHub Classroom Assistant is missing some
important functionality. It currently does not respect the deadlines of assignments, and will
only check out assignment repositories to the latest contents of the master branch at the time
of downloading. This means that if you are using Classroom Assistant, you should be very sure
to check the timestamp of the last commit.
[I've filed an Issue for this feature on their project repo, where you can view the status of 
the request as changes develop.](https://github.com/education/classroom-assistant/issues/119)

You can manage the settings from the creation step using the
_"Assignment Settings"_ button.


## Sending Assignments to Students

First, you'll need to ensure that your students are signed up with GitHub and GitHub classroom, and that
they are added to your class roster.

When students click on the assignment invitation link, they'll be prompted to create a new repository
under _your classroom organization._ This means that you (and your graders) will have full control
over their repositories, and that a student cannot make their assignment public using GitHub
(this is still possible, though).

Once some students have joined this assignment, you'll see their new repositories being created
and they'll show up on the repository dashboard.

## Gathering Completed Assignments

Once an assignment is past it's deadline, the GitHub assignment dashboard will show that the
assignment deadline has passed, and which students have submitted their assignments.

By clicking on the _"Submitted"_ button, you can view each student's repository at the time
of the submission. This is always going to be their last commit before the assignment due date.
**Be mindful of which branch/commit you are viewing**, as it is very easy to view the latest commit
on `master`, which may not be the same as the last commit before the deadline.
When grading, alwasy verify the last commit of the repo.

Students are not locked out of assignments past their due date, and retain the ability to make changes
after an assignment is due.

Assignments can be viewed in the web client, one-by-one, or with the use of the [classroom assistant tool][classroom-assistant].

### Classroom Assistant

[First, download the classroom assistant software.][classroom-assistant] Log in using your GitHub account.

After you log in, you'll be prompted to enter the assignment URL. **This is not the same URL that is sent to your students.** Instead, this is the URL of your assignment dashboard page. You can
also set this by using the "Download Repositories" button on the assignment dashboard page.

Once confirming the assignment that you wish to archive, you can select which of the student's assignments you'd like to download, and the path where they will be downloaded. Then, you can start the process. This is a very fast process, especially if you are dealing only with text.

**Note that you will be cloning the latest version of each repo from the time you've downloaded it, and not from the assignment deadline. Changes made after the deadline will appear here.**

Classroom Assistant will download projects under the following folder structure:

```
/<starting directory as specified>/<assignment title>/<student github username>/
```
It may be beneficial to require that students include their full name and student IDs in their README files,
or have a table of names and usernames.

[class-dash]: https://classroom.github.com/classrooms
[screenshot-new-indiv]: img/new-individual-assignment.png
[screenshot-recommended-indiv]: img/indiv-recommended.png
[screenshot-assignment-confirm]: img/assignment-confirmation.png
[student-pack]: https://education.github.com/pack
[classroom-assistant]: https://classroom.github.com/assistant