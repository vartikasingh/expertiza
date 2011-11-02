OSS Project 
Project E217: Integrate a few of last year’s projects
By
Chandan Apsangi (capsang) 
Vaibhav Gumashta(vgumash)
Vartika Singh (vsingh3)

E15: Notification of more kinds of events

https://trello.com/card/board/e15-notification-of-more-kinds-of-events/4e97910a88107fb718001fd1/4e979b5888107fb7180255b3

Notification should be sent for the following events:
	1)	When a new account is created, an email is sent to the id used to create the account  
	2)	When a user is assigned to review a new assignment, he/she will be sent an email informing the same
	3)	When a user is reassigned to review another assignment, he/she will be sent an email informing the same
	4)	When a user adds himself on the waiting list for a particular assignment, and later is moved off the waiting list, then an email will be sent to notify him/her about the update
	5)	When a user's work is reviewed
	6)	When author updates his work after it has been reviewed, the reviewer will be notified about the same

The commits for this project were present in two different branches on Github: E15-A and B. E15-A consists only of the commits related to E15 project. But we had to cherry-pick E15 related commits from branch B (which consists of other commits as well).

We took the following approach to integrate previous work done on Expertiza:

	1)	Create a branch E15-Notification based on 517 tag.
	2)	Merge E15-A branch into E15-Notification as all of those commits are applicable
	3)	Cherry-pick E15 related commits from branch B into E15-Notification
	4)	In case of conflicts test the feature with each of the commits separately and pick the best one.
	5)	Test each of the features listed above through local server setup
	6)	Fix any failures/make changes to ensure that the features are working
	7)	Run integration tests to ensure final quality 
	8)	Merge our branch E15-Notification with the Master

How to setup and start the application:

	1)	Create a database named "pg_development" in mysql (Mysql 5.5 database server).
	2)	Download the sql dump file. Download  the dump from courses.ncsu.edu/csc517/common/homework/OSS/expertiza-scrubbed.sql.gz 
	3)	Import this dump into the database created. To import, use: mysql -u root pg_development < expertiza-scrubbed.sql
	4)	Do rake db:migrate
	5)	Run the server.

E3: Enhancements to Suggest and Approve

https://trello.com/card/board/e3-enhancements-to-suggest-and-approve/4e97910a88107fb718001fd1/4e979b7f88107fb718025fed

Checklist:
	•	All topics on the sign-up sheet not just the student suggested ones should have a description.
	•	Students can suggest topics for approval by the instructor.
	•	Instructor can edit the topic, vote for it (Yes,No, Revise) and send it back to the student.
	•	The instructor is able to comment when accepting or rejecting, as well as when sending a topic back for revision.
	•	Once the topics are approved they should be visible in Sign-up sheet option.
	•	Should be able to sort the list by status (initiated, awaiting revision,approved, rejected).

Steps:

	1)	Created a local branch for E3, merged the relevant commits from A and B branches.
	2)	Ensured that the functionality (as listed in the checklist) is working, and lastly re-based that branch with master. 
	3)	In case of conflicts test the feature with each of the commits separately and pick the best one.
	4)	Test each of the features listed above through local server setup.
	5)	Fix any failures/make changes to ensure that the features are working.
	6)	Run integration tests to ensure final quality.
	7)	Merge our branch E15-Notification with the Master.

How to setup and start the application:

	1)	Create a database named "pg_development" in mysql (Mysql 5.5 database server).
	2)	Download the sql dump file from http://cl.ly/2C3e1u1P1E1j0V3g0z1e 
	3)	Import this dump into the database created. To import, use: mysql -u root pg_development < 517dump-scrubbed.sql
	4)	Do rake db:migrate
	5)	Run the server.
