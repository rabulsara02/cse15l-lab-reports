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

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1207201754626793512/Screenshot_2024-02-13_at_9.48.19_PM.png?ex=65dec93f&is=65cc543f&hm=0a4ed122c0f90b43c4e29e8f05b8b9ccd519e4ea6fe9ef574dde4db58af6b09c&)

# Part 2
<p>All of the prompts are within these 2 screenshots:</p>
<p> The absolute path to the private key / public key<br> </p>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1207194139146330142/Screenshot_2024-02-13_at_9.18.26_PM.png?ex=65dec227&is=65cc4d27&hm=8d1adafb506f0c1ea0d69bf64dc08a5c6a85b691ab7df6ead9d2edb45e9e22bf&)


<p>Logging in without asking for password.</p>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1207193425452077066/Screenshot_2024-02-13_at_8.59.17_PM.png?ex=65dec17d&is=65cc4c7d&hm=05958e2964ee8a74f320e90c8d889006c0d2d0148cb389c14aaf2738df0854c5&)

# Part 3:
I now know how to use ssh and the terminal from VSCdoe which is a great thing to learn. Also, I learned about terms such as ssh and scp and what they mean in the terminal and how important they can be in a job environmnet. Another thing that coincides with what I learned is also the public key that I used to ssh into the ieng6 workstation that can save time by not having to enter a password.
