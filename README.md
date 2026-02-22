# bisect

## Step 1: 
Clone down the repo - make sure git is initialized 

## Step 2: 
Add 12 different lines and commit them all seperately. (>> git add ., >>git commit -m "message")  <br>
However, change something in the second or third commit line around your 8th commit.

## Step 3: 
\>> git log --oneline <br>
\>> git bisect start <br>
open git graph

## Step 4:
Make sure you're on the most recent commit. <br>
\>> git bisect bad

## Step 5: 
Find the commit where the line that's giving you the error was added. <br>
Copy and paste the git commit ID to clipboard. <br>
\>> git bisect good b16ef53 (example ID)

## Step 6: 
It tells you the name of the commit that might be causing the error, click on that commit txt file in the bottom left git graph. <br>
Look in that file to see if the error is still there. <br>
If the error IS there do: <br>
\>> git bisect bad <br>
If the error NOT there do: <br>
\>> git bisect good <br>
<br>
Keep continuing that cycle until you found the commit that caused the error.


## Step 7: 
Now you know which commit caused the error, saving you much more time than looking through each file. <br>
To end bisect do: <br>
\>> git bisect reset <br>
It takes you back to the most recent commit.





