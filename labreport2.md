__Lab 2 Report__

*Part 1:*

Simplest Search Engine: 

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
   
    int num = 0;
    ArrayList<String> engineList = new ArrayList<String>();
    String finalOutput = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Welcome to the Simplest Search Engine!");
        } else if (url.getPath().equals("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                engineList.add(parameters[1]);
                return String.format("Added " + parameters[1] + " !", engineList.get(engineList.size() - 1 ));
            }   
        } else if (url.getPath().equals("/search")) {
            String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    for(String s: engineList){
                        if(s.contains(parameters[1])){
                            finalOutput = finalOutput + " " + s;
                    }
                }
                    return finalOutput;
            }
        }
        return "404 Not Found!";
    }
}


class SearchEngine {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

Landing Page:

This is the homepage for the Simplest Search Engine. It calls the handleRequest method for the if case of "/" and outputs "Welcome to the Simplest Search Engine!"

![SS1](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQeJz1S8yD9PJ_I_oWdYVvVIY9Fsl6KkaPM0wjNUWpvJuw9Bd87eUpNF05ycYIiU89hNMW5lmLIkCI6EVM4gUqqtuRZ6w=w1920-h901)

Add:

To add an element, the handleRequest method is called again. The "/add" in the url leads us to the first else-if statement where a String array called parameters is created that checks the remainder of the url after finding the query symbol, "?". The two parts are split by the "=" sign where the method will check if parameter[0] is "s". If so, parameter[1], the element to be added, is added into the ArrayList called engineList. The screen will print out a message notifying the user that their element has been added.

![SS2](https://lh3.googleusercontent.com/drive-viewer/AJc5JmR70wCYwj4Ls2sXCgxYoPLpGlcvtvqkOUXj4PIVj6lbQb4dAeGjqv467M31PkIMb9V24QHanjD6HXEg7g-wL3oEg3mXkA=w1920-h901)

Query:

Finally, we have the query function that again calls the handleRequest method. This time, the "/search" in the url leads us to the second else-if statement that does initially does the same thing as the first else-if statement. However, here parameter[1] is what is to be searched, so the method searches for this string in the elements in engineList and prints all the matches out. 

![SS3](https://lh3.googleusercontent.com/drive-viewer/AJc5JmQQlvExvXcIAan3mIVYSsW7UJ_e7IY5TqF1IT_DQOW6tBDhGnxVdV3-hjb8vqNbRp7cE0FGDpqqgjj8m6eoSYOGoRR0=w1920-h901)

*Part 2:*


