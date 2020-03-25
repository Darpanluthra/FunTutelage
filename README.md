# FunTutelage

1
CS 855
Final Project Write-up: FunTutelage
Darpan Luthra, CS 855, University of Regina, Student ID# 200394379
I. ABSTRACT
It is deemed that Kids do have a lot of energy and time but do not have sufficient resources to do what they want. Contrarily,
Young people do have money and energy but lack of time. Whereas, old people have time and money but not enough energy
to do all that they desire. Overall, We can conclude that throughout our life span, there is always something that restrains us
from trying something out of the box. Young/Mid-aged and old people are already habitual to a specific pattern of life, but
kids are flexible and it is said that a growing mind is a curious mind and for the same reason, this project focus on providing
resources and time management for kids. “FunTutelage” is an android application that provides a platform for communication
between teachers and students. Since kids are innocent and unaware of what is good or what is bad for them, they usually
end up wasting a lot of their invaluable time watching cartoons or unproductive YouTube videos on auto play which affects
their physical and mental growth. In solution to this, FunTutelage gives kids an opportunity to be in contact with their mentors
via a mobile interface and can do different time-bound tasks that keeps them engaged in educational and productive activities
throughout the day. Teachers can post tasks/homework from their end for students who in turn can complete the task and
upload its picture on the portal which can be viewed by the teachers. The application has been named “FunTutelage” because
learning is an ever going process, this implies it is very crucial for kids to keep themselves committed even when they are at
home during evenings or weekends for which they need someone to look after and encourage them to participate in curricular
and extracurricular activities as a tutor, hence the neme “FunTutelage: tutoring with fun”. FunTutalage is developed in Android
Studio using Java as the programming language and Google Firebase as the database. Overall, I have found that FunTutelage
is delivering a fun and interactive interface between kids and their mentors and I will add more functionality to this application
in future for making it even better in terms of accessability and usability.
II. APPLICATION DESCRIPTION
FunTutelage is an interactive day to day time management and educational android application designed to employ kids in
productive activities in order to learn something new from their phones or tablets especially when they are at home in the
evening or during weekends. I planned this application for my cousins(9 years, 5 years) with whom I live in Regina. I realized
that kids have great potential and are very quick-witted when it comes to learn something new, but they are always attracted
to animated cartoons and sometimes spend continuous 4-5 hours while watching these online shows on YouTube which is not
worth their time. The time which they can spend playing some sports, learning new skills, practicing maths or maybe doing
some recreational activity is now being wasted on a mere online show which adds no value in their knowledge. In fact, a
report[1] shows that excessive screen time either on phone or TV affects children’s mental growth and increases the chances of
health issues like obesity, diabetes, and cardiovascular issues. Not only health issues, but excessive screen time also incubates
laziness and behavioral issues in them.
FunTutelage, on the other hand, allows a mentor/teacher to make a schedule for kids. In this android application, the Teacher
is accountable to post tasks/homework on the application and its deadlines could be a couple of hours. These tasks not only
include academic assignments but can be anything that allows a kid to learn a new skill. For example, during the winter
season, mentors can ask to make a snowman in the backyard and post its picture as a submission for the task. Or sending
some downloadable links of coloring pictures which the students can print out and post it after coloring. The mentor can also
send a link to some educational videos from channels like Ted-Ed or SciShow which will indeed make them learn something
new and then they can organize a quiz based on those videos.
Since this application is being designed for small kids, the interface has been kept quite simple and eye-catching. The basic
working mechanism of this application is that new users(either teacher or student) can register themselves on the firebase
authentication server via the application interface. Once registered, the user can log in and access resources, if the user is a
teacher, they have the authority to post homework/tasks which will be saved on firebase firestore and can be retrieved by a
student user. At the same time, a student user can access the tasks posted by their teachers and after completion, the student
can post an image of it on the application which will be saved on firebase storage and only authorized teachers can have access
to it. The current version of this application has only one interface for all sorts of activities, i.e academic or non-academic,
but with upcoming versions, I will be adding different activities(pages) for different tasks.
2
III. DESIGN
FunTutelage is developed in android studio using java as the programming language and firebase as the back end database.
The concept of the application is to bridge communication between teacher and a student wherein teacher’s job is to post a
task on the application and evaluate submissions from the student, whereas student’s job is to access the task posted by the
teacher, perform it and upload an image file of that task for evaluation. In total, this application has 9 activities, which are
mentioned in Appendix A.
The application is basically divided into two streams, one is for teachers and the other is for students. On the landing
page(Appendix B)of the application, the user has to choose if they are a student or teacher. Either way, they have to log in if
they have an existing account otherwise an option to create a new user account is available which is hyperlinked to a different
activity. Once logged in, a teacher has access for posting homework or tasks on the activity page which is saved on a cloud
database in firebase firestore or the teacher can check the homework/ responses submitted by students previously in form of
images(See appendix-C) If a user is logged in as a student, in that case, the user can either see the task posted by the teacher
and after completion of the task, the user can upload an image of it on their activity page which will further be saved on the
firebase storage which is accessible by teacher(See appendix-D).
For instance, there are two users named “T” and “S”. “T” is a teacher and “S” is a student. Both have created a user account
and are now logged in to the application. The job of “T” is to provide some tasks for “S” by clicking ”Post Homework”
button. For now, we have only one module where “T” can share any kind of time-based task. Once “T” has shared a task.
“S” on a different location can see the posted task on the click of ”Retrieve homework” button. After getting the task, “S”
has to perform the given activity and click a picture of it as instructed by “T”. Now “S” can upload that picture on click of
”Submit Homework” button. Once uploaded, “S’s” job is done and now “T” can access the same data uploaded by “S” on his
application page and evaluate it accordingly by clicking on ”Evaluate previous submission” button.
IV. LIMITATIONS AND FUTURE MODIFICATIONS
Limitations: Considering the time taken to make this application, I would say the application is working pretty well and as expected,
but still, there are many areas where there are opportunities for improvement. Since the current version of this application
has only one module, Teachers have to give time-based tasks that are sometimes not attainable by all the student users as everyone
has different schedules and different priorities. If we add multiple modules like “homework”, “games”, “physical task”, “educational
videos”, etc. and post all these activities in parallel, it will be easier for students to do things as per their convenience.
Another feature that can be added to the application is a recycler view. When multiple students submit their homework, all the
image files are stored in the firebase storage, but when the teacher requests to retrieve all the submission, teacher can only view
the homework submitted by the last student. The solution to this problem is that we can call all the rows saved in storage in a list
and forward that list to mainAdapter of the recycler view where we can use Picasso library to download images and bind them to
the recycler view but considering the submission deadline date for this project I have listed this feature to be added in future improvements.
Future Modifications: For future modifications, I will be adding different modules for different kinds of tasks so that a
teacher can post all the tasks altogether for a specific date and students can perform those tasks in non chronological order
as per their convenience. Also, I will add a recycler view on the teacher’s homework evaluation page so that the teacher can
evaluate all the submissions at the same time by just scrolling on the screen.
V. CONCLUSION
After following complete software development life cycle while developing this android application, I found out that the
application is working as expected with a scope of minor changes to be made in future. It was a learning experience for
me while making my first android application in android studio. My initial idea was very ambitious but eventually I have to
settle down with some restricted functionalities keeping in mind the time available to design this application. I switched to
Java programming language after facing some difficulties with kotlin and used Firebase as a database which I was completely
unfamiliar with. I get to learn a lot of new things after a bit of struggle while working on this app, but the experience is worth it.
FunTutelage is a recreational application developed with a motive to make kids best utilize their time and it gives them
opportunities to perform and learn new things instead of spending their spare time in front of an idiot box which pretends to
be ’smart’ nowadays. This application is designed in such a way that even small kids can operate it and make their weekends
productive. The only challenge could be motivating kids to use this application regularly and for that teachers have to be very
creative and post tasks including educational fun activities which retain kid’s interest in the app and my job is to maintain it
as a responsible interface design and not adding any feature which triggers intermittent positive feedback.
During the testing phase of the application I figured out the need of some additional functionalities which I could not add
right away keeping in mind the time constraint to build this app, but I will keep working on adding more useful features and
making this application more convenient to use because kids are the future of this world and it’s our ethical duty to provide
them with sufficient resources so that they can utilize their time and energy for their overall growth.
3
APPENDIX A
ALL ACTIVITIES IN FUNTUTELAGE
Fig. 1: All Activities in FunTutelage
APPENDIX B
LANDING PAGE OF FUNTUTELAGE
Fig. 2: Landing Page
4
APPENDIX C
TEACHER’S ACTIVITIES
Fig. 3: Teacher’s Activities
APPENDIX D
STUDENT’S ACTIVITIES
Fig. 4: Student’s Activities
5
APPENDIX E
FIREBASE IMAGES
Fig. 5: Firebase Firestore
Fig. 6: Firebase Storage
6
REFERENCES
[1] University of Michigan Health System. (n.d.). Retrieved from http://www.med.umich.edu/yourchild/topics/tv.
[2] (n.d.). Retrieved from https://www.youtube.com/watch?v=r4HgdJKM5kot=284sv.
[3] (n.d.). Retrieved from https://www.youtube.com/watch?v=r4HgdJKM5kot=284sv.
[4] (n.d.). Retrieved from https://www.youtube.com/watch?v=r4HgdJKM5kot=284sv.
[5] (n.d.). Retrieved from https://www.youtube.com/watch?v=r4HgdJKM5kot=284sv.
