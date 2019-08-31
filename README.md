# Software Requirement Specification

## Product perspective

---

The EEE online community database system stores the following information:<br>

- #### Student personal information

  - Name
  - Programme and Year
  - Course Registered
  - Email, Phone number
  - Mentor-mentee pair up
  - Subscribed interest group, post,like and comment in the group
  - Anonymous questions
  - (TBC) p2p

- #### Alumni personal information

  - Student will be classified as alumni after graduation from NTU
  - Name
  - Programme and Graduation year
  - Work status
  - Job opportunity post

- #### Mentor-mentee system

  - Pair up mentor and mentee

- #### EEE faculty information

  - Name
  - Position
  - Email, Phone number
  - Office location
  - Mentor-mentee pair up
  - Current enrolling courses

- #### EEE event database

  - Stored the posted events information, including event title, date and venue
  - Stored registered students information

- #### Career information database

  - Stored the posted career event information, including event title and date
  - Job opportunities information, including job description, requirements, employer information and application deadline

- #### EEE course database

  - Course code and title
  - Current lecture/tutorial time and venue with respective lecturers/tutors
  - Anonymous questions and response

- #### Interest group database
  - Group title, built time, description, administrative and member student information
  - Events and posts

## Features:

---

1. ### Mentor-Mentee
   - Description:
     - Aims to enhance the support and communication between mentors and mentees through chat group
     - Chat group is to be formed for each mentor and his mentees, with their contact information available and updatable online
     - Support mentee’s consultations toward mentor
     - Assist mentor to identify mentee’s problems and provide guidance
     - Mentors can post an announcement or events to all, and each mentee is required to respond by clicking either Yes or No (will go or not). Mentor is able to see the result.
   - User classes and characteristics:
     - User:
       - Online communication through chat group
       - Update personal information:
         - Phone number
         - Email
         - Office location (Mentors)
     - Mentor (extended user behaviours):
       - Post event announcements to all mentees, e.g. meetings, bonding sessions etc.
       - View the announcements response results
     - Mentee (extended user behaviours):
       - Reply to the announcements, e.g. will go to the meeting, Yes/No/To be determined.
     - Admin:
       - Pair up mentors and mentees and create chat groups
       - Add mentors in their respective groups and send notifications to mentors with the group information
       - Send notifications to mentees, requiring for joining the group
       - Group administration
         - Delete the group (if a mentor quits)
         - Create new groups for new mentors
       - User data administration
   - Stimulus/Response Sequences:
     - Group invitation:
       - Users register with NTU email
       - Pop up group invitation based on the pair-up list
       - New mentees confirm to join the group
     - Announcement:
       - Mentors post an announcement with a deadline for attendance confirmation
       - Mentees reply with Y/N/To be determined
       - Mentors can view the announcement response results.

2) ### Posting questions during lectures anonymously
   - Description:
     - Aim to enhance the interaction between lecturers and students
     - All EEE modules are listed for students
     - Allow students to post questions within one module anonymously and get them solved during lectures
     - Assist lecturers to identify the students’ difficulties in this module
     - Allow users to view FAQs
     - Allow lecturers to post unique authoritative answer to FAQs
   - User classes and characteristics:
     - Lecturer:
       - Create temporary posting platform within one module, with password valid for lecture duration
       - View real time posts from students and give solutions during lectures
       - Post unique authoritative answers to FAQs
     - Student:
       - Enter the platform with password given in lectures
       - Post questions and view other questions posted by classmates during lectures
       - View FAQs and authoritative answers anytime
   - Stimulus/Response Sequences:
     - Lecturers create temporary posting platform with password before lectures.
     - Students search for the module and access the platform with the password given in the lecture
     - Students post real time questions. (Able to view FAQs when typing key words)
     - Questions are stored in database for FAQ analysis
     - At the end of lectures, lecturers close the platform, password destroyed

3. ### Internship and job search
   - Description:
     - An information sharing platform that users can access the latest career opportunities (e.g. internship, full-time jobs)
     - Student user can search for job opportunities and access application pages
     - Alumni can provide job opportunities to students
   - User classes and characteristic:
     - Student user:
       - View latest career fair information
       - Search for job opportunities via job title, job types (full-time, internship), company name
       - View job opportunities information, which includes job description, requirements, employer description, application deadline
       - Access job application page if interested in
     - Alumni:
       - Post job opportunities that open to EEE undergraduates
     - Admin:
       - Upload new job opportunities
       - Delete expired job opportunities
   - Stimulus/Response Sequences:
     - Student users search for job opportunities
     - Display a list of related uploads
     - Apply for job if interested

4) ### Broadcast EEE academic events
   - Description:
     - A blackboard for broadcasting EEE academic events in categories:
       - Technical workshops (e.g. programming, 3D printing etc)
       - Soft skill workshops (e.g. interview, presentation etc)
       - Company recruitment talk/Company visit
       - School event (e.g. EEE day, orientation etc)
   - User classes and characteristics:
     - User:
       - View EEE events in categories; in time line (latest posts)
       - Search for certain events by key words
       - Share reviews or rating after events
     - Admin:
       - Broadcast events by category
       - Filter out expired events
       - Filter improper reviews and comments
       - Clear event history semesterly
   - Stimulus/Response Sequences:
     - Users search for events in certain category
     - Display a list of events (can be filtered in latest upload)
     - Click on the registration link to secure places for events
     - Expired events are filtered out but reviews are available

5. ### Special academic interest group (e.g. AI, robotics etc)
   - Description:
     - Aim to enhance the interaction between students with similar interests, as well as assist CCA to attract more like-minded talents
     - Common interest groups should be organised by EEE official CCAs (e.g. EEE Garage/Outreach, with professor supervised), student users can join in multiple interest groups
     - Allow student users to apply for new interest groups (by voting)
     - Allow CCAs to broadcast relevant events like workshops and competitions in specific interest group
     - Allow students to share and access relevant resources, including tutorial-oriented video, open source materials, etc., and comment on the post
     - User home page shows subscribed groups and post will be shown after entering the group
   - User classes and characteristics:
     - Student user:
       - Group subscription action
         - Search for interested group
         - Preview the group description and members
         - Join or withdraw from a group, view current involved group
         - Apply for creating new groups by starting a vote, or vote for similar topics submitted by other users
         - Manage the group on their own if new groups formed.
       - Post action
         - View posts in subscribed groups
         - Posting resources, questions and comments (like/dislike feature)
         - View individual post and like on personal page
         - Report inappropriate comments and users
         - Respond to event announcements and receive confirmation
     - Admin (CCA):
       - Group management action
         - Create/delete groups
         - Change group description
         - View and administrate current group members
         - Assign more than one admin
       - Post and event action
         - Make event announcements, with external link for registration
         - Automatically send confirmation to users who successfully register for events
         - Access registration record
         - Delete/update announcement
       - Report violation
         - Maintaining group disciplinary: supervise on group members’ behaviour and report/remove member that violates disciplinary
         - Maintaining user disciplinary: supervise on users’ comments and delete improper comments
   - Stimulus/Response Sequences:
     - Joining groups:
       - Administrative creates common interest groups
       - Users search for interested groups and send joining request
       - Respective group admins accept or reject the request
         - Creating new groups (if new interest needed):
       - User starts a vote for creating groups with a new interest
       - Pending list is updated for users to vote for. A new group will be created if there are more than 30 votes.
       - Once the group is successfully created, the vote initiator is assigned as group admin.
       - Before submitting a group application, the user is required to read through the pending list, to avoid similar submissions
     - View & post:
       - Registered users click to enter the subscribed group to view posts
       - Edit their own posts/comments, like/dislike the posts
       - Respond to event announcements
       - Registration confirmation
     - Report Violation:
       - Users report violation actions
       - Administrative process on report
       - Take action (delete relevant post, comment, remove members) if needed
