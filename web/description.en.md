# CS Games 2015 - UdeS
## Web Competition
**By [Hugo Dozois-Caouette](https://github.com/dozoisch)**

### General rules

-  You have 3 hours to complete the challenge.
-  You must upload all relevant sources files on the turn-in server. No need to include the images that were given to you. Nor the libs I’m giving to you. The maximum upload size will be limited anyway.
-  You have the right to use Internet, to me a good knowledge of the web ecosystem is a big plus.
-  Completing all elements in a category gives bonus points
-  You must write a makefile that I can run using make that will build and run the server. So that I don’t have to go in each and every framework documentation to find out how to build/start it.
-  You have the right to use internet. To me, good knowledge of the ecosystem is a nice skill.
-  You must hand in a readme that lists the different functionalities implemented, this is done in order speed up correction (and make sure that I don’t forget something).
-  Be creative and enjoy!

### Introduction

It’s the end of the world as we know it… (And nobody feels fine, except R.E.M. maybe). A few years ago, a Zombie virus appeared. It didn’t appear to be really harmful and nothing was really done to counter it. However, 6 months ago, it mutated and a new race of super intelligent zombie has emerged. You are the last group of survivors and are maintained captive by a group of zombies. The chief of the horde is commanding you to create a new dating site for his son (who is not ugly enough to be popular among zombiettes).

> **spook•y** (spo͞o′kē)

>adj. spook•i•er, spook•i•est Informal

>1. Suggestive of ghosts or spirits, especially in being eerie or disturbing: a spooky attic.

*http://www.thefreedictionary.com/spooky*

### Instructions
There are a lot of functionalities. The goal is that you are not limited by the list and that you can do whatever pleases you. There’s too much stuff to be doable in 3 hours so chose well!

There is a “Hello World” of five frameworks in the folder ./src. In each folder a Makefile is available to start the server. Please note, that I don’t care which framework you are going to use and can access Internet to download anything that fits you. Just make sure to give me the procedure to run the server in the README.

As I said do not forget the README! In that file, I need the procedure to run the server, but also the list of functionality that you completed. This way I won’t forget anything! MongoDB, PostgreSQL and SQLite are installed, do not forget to give me the necessary script to create the db (if needed you can use in-memory datasets).

When zipping the file back to hand it in, you don’t have to package the images that are in ./public/default_imgs. Though, if you are using more images, do not forget to include them!

Take the time to do a quick check of the whole list before starting!

### Functionalities
####  Authentication (bonus +2 points)
-  Be able to create a new account (with the account creation page)
(+2 points)
-  Be able to log in with an account (+2 points)
-  Be able to log out (+2 points)
-  Password security (memory/database)
   -  Plain text: 0 points
   -  Encrypted/Low security hash: 1 point
   -  High security hash: 2 points

#### User Profile (bonus +3 points)
-  Have a profile with following informations (+2 points)
   -  name
   -  email (only visible on our own profile +1 point)
   -  age
   -  gender
-  Interested in (+1 point)
-  Description (+1 point)
-  Have tags (+ 2 points)
   -  Autocompletion of tags (+4 points)
-  Upload a picture (+3 points)

#### Candidate list (bonus +2 points)
-  See their names and other relevant infos (+3 pints)
-  See only the candidates of the gender I’m interested in (+1 point)
-  See only the candidates interested in my gender (+1 point)

#### Advanced candidate list (bonus + 3 points)
-  Filters:
   -  By age range (+2 points)
   -  By tags (+2 points)
   -  Being able to modify a filter in place (+2 points)
   -  have default filter that is auto-populated when doing a research (and being able to modify that default filter) (+2 points)
-  Sorting (+2 points)

#### Messaging (bonus +2 points)
-  Send an in-app message to other candidates (+3 points)
-  See the received messages (+2 points)
-  See the sent messages (+2 points)
-  See the message thread (+2 points)

####  Dates (bonus +4 points)
-  Ask someone on a date. Must contain date, place, message (+2 points)
   -  Send the date from the persone profile (+1 point)
   -  Send the date from messaging (+1 point)
-  Accept a date (+2 points)
-  See the dates I’ve sent and their status (+2 points)
-  Set your availabilities (+2 points)
-  Be able to send a date to someone only on his availabilities (+3 points)

####  Ratings (bonus +3 points)
-  Rate someone (numeric/stars etc.) on his profile (+3 points)
-  Rate someone after a date (+1 point)
-  See my rating on my profile (+1 point)
-  Comment on someone profile (+3 points)
-  Delete a comment from own profile (+2 points)

####  Likes (Facebook style-ish) (bonus +3 points)
-  Be able to like a candidate and see the people you like (+4 points)
-  See the list of people who likes us (+2 points)
   -  Be able to like the person back from the list (+1 point)
-  Have a sitewise preference so that only people that you like can message you (+2 points)

####  Notifications (bonus +4 points)
-  Notification bar/panel/page + 2 points with at least one of :
   -  likes + 2 points
   -  ratings + 2 points
   -  dates + 2 points
   -  messages + 2 points

####  Stalker Feed (events/activities) (bonus +3 points)
-  See the list of site events (+2 points) with at least one of the following in it:
   -  Likes (+2 points)
   -  Rating (+2 points)
   -  Dates (+2 points)
   -  Comments (+2 points)
-  Filter: See the activity of people I like only (+2 points)
-  See activity of someone on his profile (+3 points)

#### Bonus Functionalities

-  **Spooky**
   -  Zombie Kitten ASCII art (+2 points)
   -  Have a spooky favicon (+2 points)
   -  Have a spooky 404 page (+2 points)
   -  Have spooky music on home page (+3 points)
   -  Have a spooky cursor (+3 points)
   -  Spooky response to Konami code (up up down down left right left right b a) (+3 points)

-  **Bonus**
-  HTTPS support (nginx/apache config are accepted) (+3 points)
   -  Safe to Poodle (+1 point)
-  Mobile Friendly (+2 points)
-  Have pink somewhere (+1 point)
-  Beautiful Icons (ex: fontawesome) (+1 point)
-  Custom font (not native in browser) (+1 point)
-  JS/CSS Scripts minification (+2 points)

-  **Overall look (0-1-2 points)** (As rated by me)
