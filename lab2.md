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




