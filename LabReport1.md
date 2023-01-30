# Lab Report 1

In order to login to the *ieng6*, you will need the password. If you do not have that, you will need to reset the password first at [Password Reset](https://sdacs.ucsd.edu/~icc/index.php).

**Installing VSCode**

First go to this link here and click "Install for windows" button. [Intallation](https://code.visualstudio.com/)

![image](https://user-images.githubusercontent.com/122576152/212597779-82f0c751-0a12-468a-8a9f-17d983915c16.png)

Next proceed through the download whilst leaving everything on default. 

Once you have sucessfully downloaded VSCode, you should get a pop-up like this demonstrating completion.

![image](https://user-images.githubusercontent.com/122576152/215387866-f3f9a91e-79b3-452e-8076-688d38003243.png)

**Remotely Connecting**

Open up terminal in VSCode (located at the top middle of the appliction) and select "new terminal".
cntrl + c " ssh cs15lwi23auj@ieng6.ucsd.edu " and replace *auj* with *ieng6*
cntrl + v **OR** right click onto to the terminal to paste the copied line and hit enter.
A prompt with a " password: " should pop up. Enter the password for *ieng6* there (the text you enter will be invisible for secruity reasons).

Once you connect you should recieve this in your terminal

<img width="350" alt="image" src="https://user-images.githubusercontent.com/122576152/212205042-37682e04-a8a0-41b6-b535-4ad1ecfec4c3.png">

**Trying some commands**	

try out some of these commands once logged into the remote server. 

```
cd ~

cd

ls -lat

ls -a
```

ls <directory> where <directory> is /home/linux/ieng6/cs15lwi23/cs15lwi23abc, where the abc is one of the other group members’ username

  ```
cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
  
cat /home/linux/ieng6/cs15lwi23/public/hello.txt
 ```
  
<img width="910" alt="image" src="https://user-images.githubusercontent.com/122576152/212205220-afc4408e-5408-47a1-b1e9-d89354ef7e77.png">

cd is used to "change Directory" of the file you are refrencing. 
ls is used to "list files" of the file you are looking for. Simply, it tells you where the file is. 
cat is used to print out the contents of the file so the user can see what is inside. 
  
