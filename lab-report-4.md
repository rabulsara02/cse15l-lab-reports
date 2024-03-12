# Lab Report 4

### Task 4: Log into ieng6
<p> Simply logged into ieng6 using given command from previous labs. </p>

<br>

``` ssh rbulsara@ieng6-201.ucsd.edu ```

<br>


![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393111159635998/Screenshot_2024-02-22_at_4.46.13_PM.png?ex=65fcda6d&is=65ea656d&hm=44a5a6814def88f2c44e7ee2063561c74406350708219fbb0e406aea7dd39f48&)


<br>


### Task 5: Clone your fork of the repository from your Github account (using the SSH URL)

<p>To clone the repo from my github account, I first had to get the ssh url which was "git@github.com:rabulsara02/lab7.git". Then, once in my ieng6 space I used the command below and then hit <enter> which cloned the repository into my ieng6 workspace</p>

``` git clone git@github.com:rabulsara02/lab7.git ```

<p> I then used "cd" to get into the repo and "ls" to make sure all of the necessary files were indeed cloned.</p>

<br>


![Image](https://media.discordapp.net/attachments/1002359753957199903/1210393164137898014/Screenshot_2024-02-22_at_4.47.35_PM.png?ex=65fcda7a&is=65ea657a&hm=85fa4df05d99ddb39499a7978d0e6a298cb7cc1a018494ec95976262261fb7bf&=&format=webp&quality=lossless&width=1920&height=388)

<br>

### Task 6: Run the tests, demonstrating that they fail

``` bash test.sh```

There are test cases wtihin a file called "test.sh" which compile and run the main program. And as seen in the image below, there are failures in the test cases.


<br>

![Image](https://media.discordapp.net/attachments/1002359753957199903/1210393183557525525/Screenshot_2024-02-22_at_4.48.02_PM.png?ex=65fcda7e&is=65ea657e&hm=4a6ce617c06e5d04002bd50b4adb9f3351a7b955605272e6311f2231beb1d807&=&format=webp&quality=lossless&width=1920&height=716)


<br>

### Task 7: Edit the code file to fix the failing test

<p> In the vim editor, I used the command ":['linenumber with bug']>" to get to the right line number with the bug and then "right""right""right" arrow keys combine with "down""down" to get the the particular location of the error. </p> 

<p> Once I got to that point I clicked "i" and then changed the bug that was "index1" to "index2" then clicked "escape" </p>

<br>



<br>

### Task 8: Run the tests, demonstrating that they now succeed

<br>

![Image](https://media.discordapp.net/attachments/1002359753957199903/1210393232354181220/Screenshot_2024-02-22_at_4.48.54_PM.png?ex=65fcda8a&is=65ea658a&hm=10318c196c173e92c1f80aad596b2a63051f58aee290e6a171f473efda730e3f&=&format=webp&quality=lossless&width=1656&height=596)

<br>

### Task 9: Commit and push the resulting change to your Github account (you can pick any commit message!) 

<br>

First I used the git add command for ListExamples.java

<p> Then I used the git commit command, shown below and hit "enter"</p>

``` git commit```



<p> Then in the vim editor for the commit I first clicked on "i" and then added the message "Fixed problem in examples". And then hit "escape" and then ":wq" to write and quit and commit</p>

<br>


![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393260682649682/Screenshot_2024-02-22_at_4.49.33_PM.png?ex=65ea6591&is=65d7f091&hm=127ad7a963ed553c7eb7b3c46f9596ed80d65e46f7026cfdaffd228f2c73a0cf&)


