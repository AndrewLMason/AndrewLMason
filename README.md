# Andrew L Mason laboratory github repositories #

This is a repository for the Mason laboratory where different projects are documented and associated computer scripts are stored.

## Set up git on your computer ##
To set up Git on a Mac computer follow this guide (for other operating systems, please contact Juan Jovel: <jovel@ualberta.ca>)

1. Check whether 'git' is already installed in your computer. <br>
  2.1. Open the Mac terminal (it is in the folder Applications) and type: <br><br> 
  ```which git``` <br>
      
    if git is installed, you should see a path deployed, e.g. /usr/bin/git. If not, you have to install it:

2. Install brew. <br>
  2.2 Check if you have the program 'brew' installed typing: <br><br>
    ```which brew``` <br> 
      
    if brew is installed, you should see a path deployed, e.g. /usr/bin/brew. If not, you have to install it: <br>
    
    ```curl -fsSL -o install.sh https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh``` <br>
    ```bash install.sh```<br>
    
 3. Check again whether you have git installed. It is possible that during the brew installation, git would be installed:<br><br>
    ```which git``` <br>
    
    if installed: /usr/bin/git (otherwise is not yet installed, and you have to installed as follows:<br>
 
 4. Install git (if necessary):<br><br>
    ```brew install git``` <br>    
    (check again if git is finally installed)<br>

## Generate and set your SSH key pair ##

1. Generate SSH key, which will have the github-associated e-mail as label, type following command:<br><br>
    ```ssh-keygen -t ed25519 -C "andymasonLab@gmail.com"```<br>
    
    The following will be prompted (just press enter) <br>
    Enter file in which to save the key (/Users/masonlab/.ssh/id_ed25519) <br><br>

2. Add your SSH key to the SSH agent, with the following command: <br><br>
    ```eval "$(ssh-agent -s)"``` <br><br>
    (leave the next two questions empty, just press enter)

3. If want to visualize your private and public SSH keys, they are in the following files: <br><br>
    ```cat ~/.ssh/*``` 

4. Create config file: <br><br>
  4.1 Create file with touch: <br><br>
    ```touch ~/.ssh/config``` <br><br>
  4.2 Open config file in Mac text editor:
    ```open ~/.ssh/config``` <br><br>
  4.3 Copy and paste the following:<br>
  Host *<br>
  AddKeysToAgent yes<br>
  UseKeychain yes<br>
  IdentityFile ~/.ssh/id_ed25519<br><br>
  4.4 Save and close pop-up window<br>
  
5. Add your SSH key to Github:<br><br>
  5.1 Go to: https://github.com/AndrewLMason/AndrewLMason
  5.2 Follow instructions at: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
  5.3 When you are promted to enter your public key, visualize it (and copy it with COMMAND + C): <br><br>
    ```cat ~/.ssh/id_ed25519.pub```
  
## Clone your repository into your local computer ##

```git clone git clone https://github.com/AndrewLMason/AndrewLMason.git```




    

## List of available repositories ##

* MappingIntHBRV


<!---
For questions about this repository please write to andymasonLab@gmail.com--->
