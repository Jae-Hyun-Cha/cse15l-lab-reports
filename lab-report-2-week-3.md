# Lab Report 2 (Week 3)

# _Part1 : Search Engine_

This code shows the implementation of a simple Search Engine.

```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> SearchList = new ArrayList<String>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("");
        } else if (url.getPath().equals("/add")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")){
                SearchList.add(parameters[1]);
                return String.format(parameters[1] + " is Added.");
            }
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/search")) {
                String Searched = "";
                String[] parameters = url.getQuery().split("=");
                for(int i = 0; i < SearchList.size(); i += 1){ 
                    if (SearchList.get(i).contains(parameters[1])){ 
                        Searched = Searched + SearchList.get(i) + " ";
                    }
                }
                return Searched;
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


   - By using .getPath( ), .equals, .contains, the path is being checked and accessed.
   - First, the method will check the path _“/”_ and if it is recognized it will execute the _if_ statement.
   - Next, the method will check the path _"/add"_ and if it is recognized it will execute the _else if_ statement.
   - Lastly, inside the _else_ statement, if the method recognizes _"/search"_ then it will execute the _if_ statement inside the _else_ statement.

![Image](anewstringtoadd.png)![Image](apple.png)![Image](pineapple.png)

- In these three Screenshot, the method "handleRequest" is called and it takes _"URL"_ as a parameter.
- The method has recognized the path _"/add"_ and it will execute the _else if_ statement.  
- Like the screenshots above, the _String_ value "anewstringtoadd", “apple”, and “pineapple” gets added to the _String_ ArrayList called "SearchList" which I made inside the class. 


![Image](applepineapple.png)

- Since the "/search" the path, the method will recognize it and execute the _if_ statement inside the _else_ statement. 
- Right now, inside the ArrayList "SearchList", three String values are added. "anewstringtoadd" at index 0, "apple" at index 1, and "apple" at index 2.
- The method will search what is after "_=_" which is "app". Empty string is created to add the result. After that using the _for loop_. it will check each String value in the ArrayList "SearchList". If it recognizes that the String value has "app", it will append the String value into a single string and print it out.
- Since "apple" and "pineapple" are the String value that contains "app", "apple pineapple" will be printed.

# _Part2 : Debug_

## 1. reversed
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
``` 

- The failure-inducing input (the code of the test)
```
  @Test
  public void testReversed() {
    int[] input1 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input1));
  }
```
- The symptom (the failing test output)

- The bug (the code fix needed)
- Then, explain the connection between the symptom and the bug. Why does the - bug cause that particular symptom for that particular input?

2. append
- The failure-inducing input (the code of the test)
- The symptom (the failing test output)
- The bug (the code fix needed)
- Then, explain the connection between the symptom and the bug. Why does the bug cause that particular symptom for that particular input?