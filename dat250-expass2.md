# Experiment 1:

My first problem arrived when I was going to install lombok. My editor would not start building and I had to uninstall lombok, after that it would build no problem. Unfortunately I did not find a solution to this problem.

Second issue was with JUnit. I had problems with installing it, using maven to install the surefire and failsafe plugin. After adding it to dependencies, build, installing the files and removing it from the test scope, then updating maven settings. I managed to get it working.

After that I had some issues to run the program but after updating dependencies and readding test, as well as updating maven project from eclipse, it seems to be fixed.

**In order to run ex1 jpa, you have to go into the persistence file and remove the comments around all no.hvl.dat250.jpa.model files**

# Experiment 2

This also posed a few issues. I had trouble running it at first, but this was down to changing todos to Bank which I later fixed by going into the persistence file.

Now the databases would not run as it primary key could not be null. This was changed by adjusting the generation type to AUTO or SEQUENCE. I went with auto but found out later that sequence also works.

I also had issues running both EX1 and ex2 simultaneously due to same names. I could have changed it but did not have time to extensively test this before the deadline. Due to this I commented them out in the persistence file.

I inspected them halfly using the IDE to create tables and then querries. I could have used SQuirreL SQL but did not have enough time.
tables created were: 
* Address
- id, street, number, FK Person
* Bank
- id, name, credit
* Credit Card
- id, number, limit, balance, FK Person
* Person 
- id, firstname, lastname, FK address, FK creditcard
* Pin
- id, pincode, count FK credit card.

FK = Foreign key

# Issues

This assignment had a lot of issues for me, more than I mentioned here as I only mentioned the time consuming one.
Pending issues are derbydb inspection to see if my relations are accurate (they are coded in). JUnit still seems to not work as it should as I do not get any tests but it runs and I'm not sure exactly what to expect.
Still need to fix lombok by potentially not using eclipse as my IDE. 

output of databases
https://imgur.com/mGVUvRs

github link to both projects:
https://github.com/metrolink/dat250-jpa-example
