## 4.Log into ieng6
![Image](lab4-ex-1.png)


I pressed  ssh< space >cse15lsp23bo@ieng6.ucsd.edu , and then I pressed< enter >. This time I directly log in without ask for password since I set the SSH key. The input is to show the account name I am tring to log in, then enter to ensure. 

  
## 5.Clone your fork of the repository from your Github account
![Image](lab-4-ex-2.png)
  
  
I pressed  git<space>clone<space>git@github.com:Leaveer/lab7.git , end with <enter>. It run the cloning and finish.
  
  
## 6.Run the tests, demonstrating that they fail
![Image](lab4-ex-3.png)
  
  
First I eneter cd<space>lab7 , end with<enter> , this is to change the directory in to the file lab7, enter is to run it. 
  
  
Then I enter bash<space>test.sh , end with<enter> , to test. I came with ERROR. I also could us javac and java to test it.


## 7.Edit the code file ListExamples.java to fix the failing test (as a reminder, the error in the code is just that index1 is used instead of index2 in the final loop in merge)
![Image](Report-4-5.png)
  
  
First I enter vim ListExamples.java ,end with<enter>. This is to enter the vim mode of the file to make change
  

![Image](Report-4-6.png)
  
  
Then I enter 43j : to jump to the 43th line
  
  
11l : to jump to the 12th characters
  
  
x : to delete the current character
  
  
i : enter the edit mode
  
  
2 : add "2"
  
  
esc : exist the edit mode
  
  
:wq : save the change and quit

  
## 8.Run the tests, demonstrating that they now succeed
![Image](Report-4-7.png)
  
  
Then I enter ./test.sh ,end with<enter>. This is to run the test.sh under the current file.
  
## 9.Commit and push the resulting change to your Github account
![Image](lab4-ex-4.png)
  
  
First I enter git<space>add<space>ListExamples.java,end with<enter>. To add java file, since I have made the key and clone with ssh link, I don't need username and password in those steps. 
  

Then I enter git<space>commit<space>-m<space>"edited",end with<enter>.  To commit it. 
  
  
Then I enter git<space>status to check the status, make sure its changed.
  
  
Then I enter  git<space>push ,end with<enter>. To push it.
