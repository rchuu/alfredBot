Alfred Bot

Objectives:

Understand what methods are in Java
Be able to import a class into your project.
Understand how to use a file with the main method to test your code
Use the java.util.Date class.
Practice using String class methods
Practice using conditional control structures in Java.
Bruce Wayne's loyal and tireless Butler and best friend, Alfred is getting ready to take some vacation time. He needs to program the Batcomputer to assume his duties through a fully robotic avatar. Although he has mastered numerous arts such as rose breeding, various fields of engineering, nanotechnology, and biotechnology, he doesn't feel like programming his own conversational responses. Therefore, he has contracted you to implement the AlfredQuotes library class. It must rival the "largely unhelpful Alexis", a talking home appliance that Master Wayne bought on Tropics, a large online retailer. To the bat-code!


Java Methods

Let's review how we defined functions in JavaScript, in this low-res photo from the past:


In this case, we're going to be creating an Alfred Quote's library, a class that will have all of the functions associated with the Alfred bot's verbal responses. Because those functions belong to Alfred Quotes, they are called methods. A method is what we call a function in Java and in Object Oriented Programming generally (more on that later!) Specifically it's a function that belongs to a class. Let's break down what methods look like in Java:


For now, just include the public modifier. We'll learn more about that later.

java.util

Throughout this stack you will need to import classes from the java.util library. It contains many of the datatypes we will use later in the stack like List, ArrayList, HashMap, as well as useful classes like Random and Date to generate pseudo-random numbers.

You Will Need 2 Files:

alfredBot/AlfredQuotes.java
First, you'll need an AlfredQuotes.java file that will hold all of the AlfredQuotes functionality. This is where you will do your coding for this assignment. You won't need to compile or run this file directly, as it will be compiled by the AlfredTest.java file. We will also only call/invoke AlfredQuotes methods from within the AlfredTest.java file which is provided.

import java.util.Date;
public class AlfredQuotes {
     /*
    * Inputs: None
    * Return Type: String
    * Description: Returns a generic greeting that Alfred will say to anyone.
    */
    public String basicGreeting() {
        // You do not need to code here, this is an example method
        return "Hello, lovely to see you. How are you?";
    }
    
    /* 
    * Inputs: String name, String dayPeriod 
    *                      Assume "morning", "afternoon" or "evening".
    * Return Type: String
    * Description: Returns a greeting that includes the person's name
    *         as well as the day period. For example:
    *        "Good evening, Beth Kane. Lovely to see you."
    * Tip: Try using the String.format method for string interpolation in Java.
    */
    public String guestGreeting(String name, String dayPeriod) {
        // YOUR CODE HERE
        return "place holder for guest greeting return string";
    }
    /* 
    * Inputs: None
    * Return Type: String
    * Description: Returns a polite announcement of the current date.
    */
    public String dateAnnouncement() {
        // YOUR CODE HERE
        return "place holder for date announcement return string";
    }
    
    /*********************************************
    Final Challenge!
    Alfred is listening. Write a method that accepts any string of conversation. 
    If "Alexis" appears in the conversation return a snarky response, such as:
    "Right away, sir. She certainly isn't sophisticated enough for that." 
    
    If "Alfred" is in the conversation return an obliging response, for example: 
    "At your service. As you wish, naturally." 
    
    If neither name is found, return an appropriate response, for instance:
    "Right. And with that I shall retire." 
    **********************************************/
    /*
    * Inputs: String (A conversation)
    * Return Type: String (Something Alfred would say in response)
    * 
    * Tip: Use the indexOf String method
    */
    public String respondBeforeAlexis(String conversation) {
        // YOUR CODE HERE
        return "place holder for snarky response return string";
    }
    // NINJA BONUS
    // Write your own AlfredQuote method using any of the String methods you have learned!
}
copy
alfredBot/AlfredTest.java
The methods that belong to the AlfredQuotes file do not execute automatically without the test file. For our Java assignments in this section going forward, you will have two files. But you will only need compile and run the test file, which will compile the other file as well if there is an instance of that class in the test code. You do not need to alter this file, although you may if you like.

public class AlfredTest {
    /*
    * This main method will always be the launch point for a Java application
    * For now, we are using the main to test all our 
    * AlfredQuotes methods.
    */
    public static void main(String[] args) {
        // Make an instance of AlfredQuotes to access all it's methods.
        AlfredQuotes alfredBot = new AlfredQuotes();
        
        // Make some test greetings, providing any necessary data
        String testGreeting = alfredBot.basicGreeting();
        String testGuestGreeting = alfredBot.guestGreeting("Beth Kane", "evening");
        String testDateAnnouncement = alfredBot.dateAnnouncement();
        
        String alexisTest = alfredBot.respondBeforeAlexis(
                            "Alexis! Play some low-fi beats."
                            );
        String alfredTest = alfredBot.respondBeforeAlexis(
            "I can't find my yo-yo. Maybe Alfred will know where it is.");
        String notRelevantTest = alfredBot.respondBeforeAlexis(
            "Maybe that's what Batman is about. Not winning. But failing.."
        );
        
        // Print the greetings to test.
        System.out.println(testGreeting);
        
        // Uncomment these one at a time as you implement each method.
        // System.out.println(testGuestGreeting);
        // System.out.println(testDateAnnouncement);
        // System.out.println(alexisTest);
        // System.out.println(alfredTest);
        // System.out.println(notRelevantTest);
    }
}copy
A Note About Commenting Your Code

As you go through this bootcamp, it's a good idea to use comments liberally. Not only will you make your own life easier, but down the line, if you're working on a project and someone else ends up maintaining your code, they will thank you for well-commented code. Likewise, you will appreciate well-commented code in any project you inherit. Many teams and companies will have a style guide for commenting code that you will need to adhere to. In fact, commenting code can also contribute to the autogeneration of documentation in human-readable form. If you're curious about a tool the JDK uses to do this, check out the link for an intro to Javadoc below.

Useful Links

java.util
Java String documentation
Javadoc

Create a project folder in your Java stack folder called "alfredBot"

Create an AlfredQuotes.java class file that will hold all of Alfred bot's functionality.

Create an AlfredTest.java main program file that will execute code to test our AlfredQuotes class.

Implement the guestGreeting method, and test it by first compiling the test file with the javac command and then running the test file with the java command in your terminal.

Implement the dateAnnouncement method, and test it.

Implement the answeringBeforeAlexis method, and test it.

NINJA BONUS: Implement your own method for the Alfred bot using any of the built-in String methods you've learned. Maybe he can yell..