# Part 1
`import java.io.IOException;
import java.net.URI;
`
`class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String mySearch = new String ("Hi!");`

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return mySearch;
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    mySearch = mySearch + "\n" + parameters[1];
                    System.out.println();
                    return mySearch;
                }
            }
            return "404 Not Found!";
        }
    }`
`}
class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }`

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
`}`

# Part 2
I used edstem for this part and plan to redo this entire lab through my local machine.

# Part 3:
I still need to go over on how to create a webserver through Java, but I now know how to use ssh and the terminal from VSCdoe which is a plus.
