Lab Report 2  

Part 1:  

This is my code for my StringServer:  
 
    import java.io.IOException;
    import java.net.URI;

    class Handler implements URLHandler {
        String input = "";


        public String handleRequest(URI url){
            if(url.getPath().equals("/")){
                return String.format("This is your string : %s", input);
            }
            else{
                System.out.println("Path: " + url.getPath());
                if(url.getPath().contains("/add-message")){
                    String[] parameters = url.getQuery().split("=");
                    input += parameters[1] + "\n";
                    return String.format("Your string has been updated! Its now this: \n%s" , input);
                }
            }
            return "404 Not Found!";
            
        }


    }

    class StringServer{
        public static void main(String[] args) throws IOException{
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 to 49141");
                return;
            }
            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }  
   
This is the first screenshot of using the `/add-message` command in the String Server:  
![Image](StringServercmd.png)  

For this first add-message command the first method that is called is the main method in order to start up the server. Then once it has been started, the handleRequest method is called when the URI url has "/add-message"; particularly the else statement of this method. When "/add-message" is used in the command line, the URI url parameter is split by the "=" sign. The index 1 argument is the message that is added to the `String input` field that was initialized before the method. Additionally, after the string is added a new line is also added to prepare a new line for any new strings. Before the /add-message command was used, the `input` field was just an empty string. The input field was changed because it was an empty string when it was initialized and after the method call there is not a new string added to it.  

![Image](StringServercmd2.png)  

For this second add-message command, the main method is not called again because the server is already running and was not stopped in this case. The handleRequest method is called, particularly the else statement. Again, the URI url is split by the "=" sign and the index 1 argument becomes the string that is added to the input field. Instead of being an empty string, the string already contains the string we added previously: "Data". Now this field is changed and "Structures" is added to the string on a new line.  

Part 2:  
The bug I am choosing to analye is the bug within the Reversed method in the ArrayExamples.java file. The purpose of this method is to create a new array and copy over elements from a given array to the new array in reverse. The bug in this method is that it always returns an array full of zeros. This is because instead of copying over elements from the given array to the new array, this method does the opposite. It copies elements from the new empty array to the given array which results in an array full of zeros.  

Junit failure-inducing test:   

    @Test  
    public void testingReverse(){  
        int [] input1 = {1,2,3,4,5};  
        assertArrayEquals(new int[]{5,4,3,2,1}, ArrayExamples.reversed(input1));
    }  
This test will fail because the ArrayExamples method returns an array full of zeros.  

Junit non-failure-inducing input:  

    @Test
    pulic void passTestingReverse(){
        int[] input1 = {0,0,0,0};
        assertArrayEquals(new int[]{0,0,0,0}, ArrayExamples.reversed(input1));
    }  
This test will pass because the array that is returned is always full of zeros. So a given array full of zeros will match the resulting array full of zeros as well.  

Symptom:  

Output of first test:  
![Image](



Before code (bugged):  

    static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
          arr[i] = newArray[arr.length - i - 1];
        }
        return arr;
      }
After code (debugged): 

    static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
          newArray[arr.length - i - 1] = arr[i] ;
        }
     return newArray;
      }  

The difference between theb before and after code is that the after code is setting elements in the new array equal to those in the given array. The after code now also returns the newArray instead of the given array arr. 




Part 3:  
In this lab I overall learned a lot about web servers and URLs. I learned about the different parts of a URL and how they affect what is displayed on a web server. I also learned how to write the code to start up a simple web server and how to add a command that would change the web server with queries and strings. 


