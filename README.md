StudyLink is an app that helps IE University students find the most compatible study partners based on degree, classes, availability, campus, and preferences.

It uses data structures such as dictionaries, sets, and binary heaps, to compute real-time compatibility scores and return the top 3 matches directly.

# Description #

StudyLink solves a real problem among IE students: it allows users to connect with other IE students, ensuring a safe and productive study session.

Through a simple console interface, StudyLink allows students to:

1) Create a personal profile (degree, campus, classes, schedule, preferences)

2) Store that data efficiently using dictionaries

3) Compare similarities using set intersections

4) Rank possible study partners using a binary heap

5) Retrieve the top 3 most compatible classmates instantly

# Why these algorithms #

dictionaries (O(1)): very efficient for storing and accessing user profiles quickly

sets (fast intersection): perfecy to compare shared classes and schedules

binary Heap (O(log n) priority queue): efficient structure to rank that always keeps best matches on top

Challenges faced:

* Designing a just and weighted scoring method

* Building a custom heap (instead of using heapq)

* Managing user input cleanly within the console itself

* Ensuring the system that matches adapts and scales as more profiles are added

Future features:

* Replace console UI with a web or even a mobile interface

* Real database (such as JSON or even SQL) to store profiles permanently when app is closed 

* Inside app call options + ratings

* Filters by study habits or academic strengths

* Integration with IE login or schedule systems

# How to install and run the project #

no need to type any terminal commands, just follow these simple steps:

Step 1: Download ZIP
(Click on the green code -> download ZIP button on GitHub)

Step 2: Extract
(Unzip the folder to your desktop or documents)

Step 3: Run
(Double-click: ads.py-> the program will open in your python environment (in the editor window, you will have to click on run (F5 button on MacOS)))

# How to use the project #

When the program starts, you will see:

1) Create user
2) Show matches
3) Quit

for option 1: create user

You will enter:

* Username

* Degree

* Campus

* Classes (comma-separated)

* Availability (comma-separated)

* Preferences (comma-separated)

Your profile is then stored in the system dictionary

for option 2: show matches

* Enter your username

* Program computes compatibility with all other users: uses dictionary + scoring + heap ranking

Displays:

* Match: eva – score: 17
* Match: nour – score: 15
* Match: hiro – score: 14

for option 3: to quit

* simply exits the program

# Features (MVP) #

* Console based user interface 

* User profile creation

* Course and availability comparison using the set intersections

* Compatibility scoring

* Ranking with binary heap

* Returns top 3 best matches

* Works entirely offline

* No external libraries required

# Algorithm #

For StudyLink, we created a matching algorithm that helps students find the most compatible study partners. The idea is to compare one student with all the other students in the system and decide who fits best based on several factors. To organize the information, we store every student in a dictionary, where each profile includes their degree, the classes they take, their available study times, their campus, and their study preferences. These pieces of information are kept in sets because sets make it easy and fast to compare similarities, such as checking how many classes two students share.


When a student asks for matches, the algorithm looks at every other student and calculates a compatibility score. This score becomes higher when two students take the same classes, have overlapping time slots, share the same campus, or have similar study preferences. Each of these similarities contributes to the final score. This scoring step helps us measure how strong the connection between two users is.


After the score is calculated, we place it inside a binary heap. A binary heap is a structure that always keeps the best-scoring users at the top. This helps us avoid sorting the entire list of users every time. By using the heap, we can quickly find the most compatible study partners without doing extra work. Once all the possible partners have been evaluated, we take the top results from the heap. These top results represent the students with the highest compatibility scores.


This algorithm works well because it uses efficient data structures. The dictionary allows fast access to each user, the sets let us compare information quickly, and the binary heap helps us retrieve the best matches without wasting time. The overall process is efficient and grows well even if many students use the app. This makes it a practical and effective solution for StudyLink.

# Files explained #
**ads.py**	our main program: containing user cretion and management, the scoring logic, heap ranking algorithm, annd the menu

**README.md** the document containing the explanation of how to install run and understand the full project

**ux_tests/**	the folder designed for our UX test video recordings

**resources/** for some of the additional files such as test data (test users' file to test the program)


# Prerequisites & Environment #

* Python 3.9+

* Works on: macOS, Windows, Linux

* No external libraries required

* Just double-click to run

# Further Improvements #

* Move from console user interface to web GUI 

* Permanent database for user storage 

* Make scoring model better with more attributes

* Add filters for degree, campus, study habits

* Implement real chat user interface and in app calling options

* Integrate with IE email login

# Credits #

StudyLink Development Team:

Nour Ben Haj Hassine — Project lead, UX, storytelling, pitch, inception deck

Eva Gomez — UI/UX mockups, app visuals, pitch presenter

Hiroyuki Sen — User stories, algorithm testing

Ismail Benabdallah — Coordination, pitch presentor, business model

For the course Algorithms & Data Structures of IE University in 2025
