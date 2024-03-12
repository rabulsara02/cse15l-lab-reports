# Lab Report 4

### Task 4: Log into ieng6
<p> Simply logged into ieng6 using given command from previous labs. </p>

<br>

``` ssh rbulsara@ieng6-201.ucsd.edu ```

<br>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393111159635998/Screenshot_2024-02-22_at_4.46.13_PM.png?ex=65ea656d&is=65d7f06d&hm=b2432a9550208bf3bc5417715a72788207a6c6a4b02f75a613e8212213d937eb&)

<br>


### Task 5: Clone your fork of the repository from your Github account (using the SSH URL)

<p>To clone the repo from my github account, I first had to get the ssh url which was "git@github.com:rabulsara02/lab7.git". Then, once in my ieng6 space I used the command below and then hit <enter> which cloned the repository into my ieng6 workspace</p>

``` git clone git@github.com:rabulsara02/lab7.git ```

<p> I then used "cd" to get into the repo and "ls" to make sure all of the necessary files were indeed cloned.</p>

<br>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393164137898014/Screenshot_2024-02-22_at_4.47.35_PM.png?ex=65ea657a&is=65d7f07a&hm=2c568d97df486b3db5df2abe12678e98e8e4295b04c39f8b711fa4075cc6c9aa&)

<br>

### Task 6: Run the tests, demonstrating that they fail

``` bash test.sh```

There are test cases wtihin a file called "test.sh" which compile and run the main program. And as seen in the image below, there are failures in the test cases.


<br>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393183557525525/Screenshot_2024-02-22_at_4.48.02_PM.png?ex=65ea657e&is=65d7f07e&hm=926910aa5824045809dc38cb36a31f379fbcf3627913a671231aae648e59d2cb&)

<br>

### Task 7: Edit the code file to fix the failing test

<p> In the vim editor, I used the command ":['linenumber with bug']>" to get to the right line number with the bug and then "right""right""right" arrow keys combine with "down""down" to get the the particular location of the error. </p> 

<p> Once I got to that point I clicked "i" and then changed the bug that was "index1" to "index2" then clicked "escape" </p>

<br>

![Image](INSERT)

<br>

### Task 8: Run the tests, demonstrating that they now succeed

<br>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393232354181220/Screenshot_2024-02-22_at_4.48.54_PM.png?ex=65ea658a&is=65d7f08a&hm=f431ee9206bd4bad7a51c493e93acb7302cf6ca37e508694cc4b24521f3636e3&)

<br>

### Task 9: Commit and push the resulting change to your Github account (you can pick any commit message!) 

<br>

First I used the git add command for ListExamples.java

<p> Then I used the git commit command, shown below and hit "enter"</p>

``` git commit```



<p> Then in the vim editor for the commit I first clicked on "i" and then added the message "Fixed problem in examples". And then hit "escape" and then ":wq" to write and quit and commit</p>

<br>


![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1210393260682649682/Screenshot_2024-02-22_at_4.49.33_PM.png?ex=65ea6591&is=65d7f091&hm=127ad7a963ed553c7eb7b3c46f9596ed80d65e46f7026cfdaffd228f2c73a0cf&)


