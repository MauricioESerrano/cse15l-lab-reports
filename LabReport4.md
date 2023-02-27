# Lab Report 4

**Step 4**

```
ssh cs15lwi23auj@ieng6.ucsd.edu
<enter>
```

These keys allowed me to first login to the remote server.

![image](https://user-images.githubusercontent.com/122576152/221480709-b27e3f65-87ad-4c91-92d6-bbb6c0d72dbc.png)

**Step 5**
```
<cntrl + c> https://github.com/ucsd-cse15l-w23/lab7.git
```
```
git clone <right click> 
<enter>
```

This allowed me to clone the repo to my ssh

![image](https://user-images.githubusercontent.com/122576152/221481129-7c6b52d6-deb7-44c9-891a-9ae4fea68f2d.png)

**Step 6**

```
cd l <tab>
<enter>
<shift + insert>
<enter>
<shift+insert> <space> L <tab> T <tab> <backspace>
<enter>
```

We go into the new repo. Then paste the javac and java command to run the Test files to demonstrate failure. 
Then the next paste has to do with the  key presses after that autocomplete and <backspace> to remove the . to get ListExamplesTest.
  
![image](https://user-images.githubusercontent.com/122576152/221481697-1ab9f951-6529-426f-8f42-3b82d7826831.png)
  
**Step 7**
  
```
vi L <tab> . < tab>
<right> i <backspace> 2 <esc>
:x
```

vi & L auto completes with the tab to open ListExamples then the . tab again to java. Vi allows us to edit the file. Vi to the problematic portion, in this case index1 to index2.
You go right then i to edit and backspace to delete and replace with 2. escape with esc and :x to save and exit.
  
 ![image](https://user-images.githubusercontent.com/122576152/221482124-5e8ed76c-7a32-4e25-b8bf-a38a62af82f4.png)
  
  **Step 8**
  
  ```
<shift+insert>
<enter>
<shift+insert> <space> L <tab> T <tab> <backspace>
<enter>
```
This is basically a repeat of step 6 where you compile and run the tester.

![image](https://user-images.githubusercontent.com/122576152/221482304-2addd3ff-6634-433c-9a41-6a8816731cc3.png)

**Step 9**
  
```
git add L <tab> j <tab
<enter>
git commit -m "finished"
<enter>
git push
<enter>
```
  
![image](https://user-images.githubusercontent.com/122576152/221482652-3abcadc5-c1ac-4f4a-83eb-4187178d3e68.png)
  
This adds ListExamples.java and commit with message of "finished". Then you git push.







