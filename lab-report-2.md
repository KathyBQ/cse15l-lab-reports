Part 1:
1. two screenshots of using /add-message for StringServer
   ![Image](strser1.png)
   ![Image](strser2.png)
3. for each of the 2 screenshots, describe:
   - which methods in your code are called?
        It called handleRequest, getPath(), getQuery(), contains() methods.
   - what are the relevant arguments to those methods, and the values of any relevant fields of the class?
        - handleRequest(URI url): the parameter is a url. have an int num and a string content variables to go through this method to record the previous and the current line number and the updated line messages. 
        - getPath(): url.getPath().contains("/add-message"), get the url's path, and then check if it contains the string "/add-message".
        - url.getQuery().split("="): get the query from the url, and then split the equal sign.
     
   - how do the values of any relevant fields of the class change from this specific request? if no values got changed, explain why.
        When checks the path has "/add-message?s=something", the line number ```num``` will be increased by 1, and the adding message ```something``` will be concatenated to the previous string object ```content``` with corresponding line number.

Part 2:
1. the path to the private key for your SSH key for logging into ieng6 on the computer: ```/Users/binqiliu/.ssh/id_rsa.pud```
2. the path to the public key for the SSH key for logging into ieng6 within your account on ieng6: ```/home/linux/ieng6/cs15lfa23/cs15lfa23ti/.ssh/authorized_keys```
   
   ![Image](generate-key.png)
   ![Image](private-key.png)
   ![Image](keys.png)
   
   Without password to log in the ieng6:
   ![Image](public-key.png)

   ```ls``` list the folders and files under my ieng6:
   ![Image](ls-ieng6.png)


Part 3:

   I didn't know ssh, curl, and scp before. I learned how to create an easy server in java and how to use the commands on the terminal to remotely compile/control my programs. 

