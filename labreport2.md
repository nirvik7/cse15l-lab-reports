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
