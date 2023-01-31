# LAB 2 REPORT

In this report, I will be showing how I implemented a web server called StringServer--which tracks String added by incoming requests and prints them onto 
the front page of the web server--and my analysis of a buggy program using Junit testing.

# PART 1
 
Below is my code for the StringServer web server 

```import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String returnString = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format(returnString);
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                
                returnString += parameters[1]+ "\n";
                return String.format(returnString);
                
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

There are two parts to my code: Handler Class and StringServer class:

The Handler class has two if statement. If the url only has "/" then it accesses the path of the URL and return the current string. Otherwise, it would execute the else statement. This else clause states that if there is an `/add-message` command in the path, then the program should concatenate the string behind the "=" sign to the current string. Note that each string will be printed on its own line when on the web server.

The StringServer class' main point is to set the port number that should be entered in when the class is called in the terminal, and launch a webserver with the port number. For instance, when we run java NumberServer 4000, the program starts a web server at port 4000 that the local host connects to.

Here are my examples of using `/add-message`:

![image](use1.png)
In this example, I created a web server with port 4002. In the terminal, when I compile using `javac Server.java StringServer.java` and run immediately after using `java StringServer 4002`, the main method in the StringServer class was called and a web server that is connected to the local host with port 4002 was created. For this exmaple, when I used `/add-message,` the else clause of the if statement of the handleRequest method in the Handler class was called, causing the String "Today is a wet day" after `/add-message`, to be added into the String 'returnString'. 

![image](use2.png)
Similarly, in this instance, I created a web server with port 5000. Running the `javac Server.java StringServer.java` and `java StringServer 500` commands in the terminal in order, the main method in the StrinServer class was called, which in turn launches a new webserver that connects to the local host with port 5000. When I added the string "Happy" using `add-message` the handleRequest method was called again, allowing the string `returnString` to append "Happy"







