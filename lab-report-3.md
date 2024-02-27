# Lab Report 3

## Part 1
    
A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
```
  @Test
 public void testReverseInPlace2() {
   int[] input1 = {1, 2, 3 };
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{3, 2, 1}, input1);
 }
```
An input that doesn't induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
```
@Test
 public void testReverseInPlace2() {
   int[] input1 = {0};
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{0}, input1);
 }

```

The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
1.
![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1207096698644602930/Screenshot_2024-02-13_at_2.47.33_PM.png?ex=65de6767&is=65cbf267&hm=fd87cdc0cdd3df75ee36dd0690fd8a3ecd22dca250f606eae4cac739f94ffc7c&)

2.
![Image](https://cdn.discordapp.com/attachments/1002359753957199903/1207097504911466566/image.png?ex=65de6827&is=65cbf327&hm=a6e05f626def37ca910676a037617f036ca7aef499ed6edcda8611e90fece1df&)

The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
```
  //OLD
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```

<p>The bug above  was that the array never actually got reversed in place, instead the it started at the end and then as it got the beginning, the array just became mirrored. </p>

```
//NEW
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i += 1) {
      int current = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = current;
    }
  }
```


## Part 2
<p>I chose the grep command for this part.</p>

<p>The first option I found that can be used with grep is the grep "-i" command. </p>
<p>What this command does is it prints lines with the same word(s) after -i</p>
<p>For example, let their be a file ucsd.txt that contains the following<br> </p>

```
UCSD Rocks 
UCSD Revelle Rocks 
UCSD 64 Rocks 
UCSD Parking Sucks
```

<p>Now lets use grep -i<br>
</p>

<br>

```
grep -i rocks ucsd.txt 
UCSD Rocks 
UCSD Revelle Rocks 
UCSD 64 Rocks 
```

<p> Let's try another </p>

```
grep -i sucks ucsd.txt
UCSD Parking Sucks
```

<p>The second option I found that can be used with grep is the grep **-c** command.</p>
<p>What this command does is it prints the number of lines that contain the criteria after "-c" </p>
<p>Using the same example file ucsd.txt, let's try out "grep -c" <br>
</p>

```
grep -c Rocks ucsd.txt
3
```
<p> Let's try one more </p>

```
grep -c sucks ucsd.txt
0
```
<p>We get 0 because the -c does not ignore capitilzation, so if we did **-ci** then we would get our expected value of 1.</p>

<p>The third option that can be used with grep is the grep **-v** command.</p>
<p>What this command does is that is prints all lines that do not contain the value after **-v** in other words, the inverse</p>
<p>Using the same example file ucsd.txt, let's try out grep **-v**<br>
</p>

```
grep -V Rocks ucsd.txt
UCSD Rocks
UCSD Revelle Rocks
UCSD 64 Rocks
```
<p> The "-v" command also cares about capitilazation, so it is best to use it in conjuction with the -i command to make things easier.<br>
For example</p>

```
grep -v sucks ucsd.txt
UCSD Rocks
UCSD Revelle Rocks
UCSD 64 Rocks 
UCSD Parking Sucks
```
<p>We get everything because we didn't use the -i in conjunction</p>


<p>While there are many more command options for grep, the fourth one I would like to demonstrate is the grep **-A n**</p>
<p>This command reads the file and then prints matches 'n' lines after the match</p>
<p>Using the same example file ucsd.txt, let's try out grep **-A 2**<br>
</p>

```
grep -A 2 Revelle ucsd.txt 
UCSD Revelle Rocks 
UCSD 64 Rocks 
UCSD Parking Sucks
```
<p> Alternatively if we only want one line after, we could say</p>

```
grep -A 1 Revelle ucsd.txt 
UCSD Revelle Rocks 
UCSD 64 Rocks 
```

### [Source](https://docs.rackspace.com/docs/use-the-linux-grep-command)





