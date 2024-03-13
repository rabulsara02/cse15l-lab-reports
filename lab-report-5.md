# Lab Report 5

## Edstem

### Student Question

<p>  I am currently trying to find a .java with the most lines in a directory. I know that the wc command lets me do that, but I am getting an output for each file. <br>
  I am getting only one line that looks like this.  
  I have included my command below as well.
</p>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1217254872957849640/Screenshot_2024-03-12_at_4.16.31_PM.png?ex=66035bf1&is=65f0e6f1&hm=d3541489b99150a661c520be69c3f94b1968a96c260aa2af114171c144947355&)



### TA Answer

<p>It looks like you are using "|". To remind you, this command uses the answer from the preceding command as an input to the upcoming command <br>
  In this scenario you want to use the "-exec" commmand in conjunction with your "find", so that it executes the command per each file. <br>
  Also, since this can be confusing and we didn't talk much about this in class, you can use the + at the end of your command which tells "find" to gather the found files and run the command per file.
</p>


### Student Response

<p>Thank you! I tried using the command below and implemented the suggestions and it worked!
</p>

```find submissions/ -type f -exec wc -w {} +```

<p>Another question I had is how to approach the buggy "if" statement in my bash script.</p>

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1217285119124181073/Screenshot_2024-03-12_at_6.36.21_PM.png?ex=6603781c&is=65f1031c&hm=3bee74274148666366ab02b85784eb1646f8f55d879bbac77e191686883bb3eb&)


<p>I am not sure how to even get started with this. I remember that I need to use the format of "[[ 'condition' ]]" but do not know what to put</p>


<br>



### TA Answer

<p>Hello. You definitely got the format right! A little hint to get you going in this if statement is to check the exit code of the program when it has been run. In this assignment the exit code is necessary. <br>
  Recall on how to obtain the exit code with a certain command. <br>
  (Hint: you want to check whether the code means an error or succeeds, which number means no errors?)
</p>


### Student Response

<p> I remember that the number 0 means that the program has run without any errors. So I used the code below and it seems to work perfectly now!</p>

```if [[ $? -ne 0 ]]```

![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1217287497550139462/Screenshot_2024-03-12_at_6.45.50_PM.png?ex=66037a53&is=65f10553&hm=e6b8f58f37b3c50309e28552dfea3abea06f9cd540138fbb89a6331a6e818ac7&)

