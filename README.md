# KappaArt
##SDHacks 2016 Submission
### By: Danny Diep, John Li, Michaella Sheng, David Zhang

#The greatest thing about twitch is streamer to viewer interaction.

KappaArt is a Twitch chat bot that encourages users to create art through contests and streamer connection. It serves to provide a way for chat to have fun creating anything 
from handdrawn fanart, to a photoshopped meme based on a specified topic of choice. KappaArt bot will give a certain amount of time for
each contest, specifying the rules ahead of time and then allowing for users to draw, paint, or sketch and submit their art for the moderators and further chat voting.  


#How does it work?
The bot will hold contests and store all user submissions through parsed imgur links. Depending on the style and preference of the streamer, either they themselves or a moderator can decide what topics they would like to
have for the contestant if any. They will then set a length of time to allow chat time to create and begin the contest. Users will be able to upload their
artwork on imgur. The bot will take all posted links in chat and store them in a secure hash table until the contest is over. Afterwards mods will be able to access
the list of users and their drawings and filter or remove any inappropriate or offensive content. From there they can crown a user the KappaArtist of the stream.

#Required Software
1. [mIRC](http://www.mirc.com/)
2. [JSON For Mirc](https://github.com/SReject/JSON-For-Mirc)

#Instructions
1. Install JSON For Mirc into the ucart folder.
2. Navigate to your mIRC directory.
2. Copy the contents of the ucart folder into the mIRC folder.
3. Run mIRC, and connect to the server. 
4. Enter a channel name with #username. This channel name should match your twitch bot account.
5. Join that channel to begin typing commands and comments under that channel.

##To Make a Contest
Make sure you have a list of topics inside the topics.txt file. Make sure you start from the first line and make a new topic per new line. Once you have done so, you need to create the topic list for the bot to use. To do this, type

!createtopiclist

This will create the topics from the text file. Now, you must select a topic by using either !selecttopic or !selectrandomtopic. You can use !listtopics to list the current topics loaded.

After selecting a topic, you should select a time. Use !timerset to set the time in seconds. Once you have both a topic and time set, you are able to start the contest by using !startcontest.

##Getting User Information
During a contest, users will be passing in links which the bot will store into a hash table. This occurs until the end of a contest. Mods and the stream themself can access the user information through !getinfo. This command will display everyone's submission with a particular ID. You can announce the winner by using !announcewinner ID once you find out who the winner is. 

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
