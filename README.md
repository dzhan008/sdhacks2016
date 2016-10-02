# UCArt
##SDHacks 2016 Submission
### By: Danny Diep, John Li, Michaella Sheng, David Zhang

#What is UCArt?

UCArt is a Twitch chat bot that creates art contests amongth users. It serves to provide a way for chat to have fun creating different
art pieces of either random moments of their favorite streamer, or a specified topic of choice. Depending on the amount of time given for
each contest, people can enjoy themselves rushing to make a quick doodle of their streamer or wait until they can create a masterpiece to
showcase. It allows for interactivity between the users and helps produce more art content in the stream. 


#How does it work?
The bot will hold contests and store all user submissions through links. The streamer or moderator can decide what topics they would like to
have for the contestant, and they can specify however long they want it to be. When the contest starts, users will have to upload their
art pieces on imgur. The bot will take all posted links in chat and store them until the contestant is over. Mods will be able to access
the list of users and art pieces and be able to filter it out themselves. They or the streamer can choose a user and be crowned the artist
of the stream.

#Requirements
1. [mIRC](http://www.mirc.com/)

#Instructions
1. Navigate to your mIRC directory.
2. Copy the contents of the ucart folder into the mIRC folder.
3. Run mIRC, and connect to the server.

#Commands

###Contest

!timerset <seconds>

Sets the contest duration in seconds.

!startcontest

Starts the contest with the given parameters.

!stopcontest

Stops the current contest.

!announcewinner <id>

Announces the winner of the contest for the given person's id.
 
###Topics

!createtopiclist

Creates a new list of topics from the external text file.

!listtopics

List all topics.

!selecttopic <id>

Select a topic based on the id.

!selectrandomtopic

Selects a random topic from the list.
 
###Contestant Data

!save

Saves recent contestant data into the a text file.

!load

Loads the data saved from the text file into a hash table.

!reset

Resets the hash table that stores all the recent contest information. Use only if you want to start a new contest or if something is wrong with saving, loading, or getting contestant information.

!getinfo

Grabs all pooled information from a recent contest.
