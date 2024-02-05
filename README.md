**Q 1 : Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.**
```
cd /home/
```
```
sudo mkdir MyFiles
```
```
ls
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/b94a4d10-e661-489c-9b3d-32f198f6d759)

**Q.2 Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."**
```
sudo touch document.txt
```
```
cd MyFiles/
```
```
ls
```
```
cd /home/
```
```
ls
```
```
sudo cp document.txt MyFiles/
```
```
cd MyFiles/
```
```
ls
```
```
sudo mkdir Document
```
```
ls
```
```
cd ..
```
```
sudo mv MyFiles/document.txt MyFiles/Document
```
```
ls
```
```
cd MyFiles/
```
```
ls
```
```
cd Document/
```
```
ls
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/105c4342-e309-46a7-bcb8-5841adba8124)


**Q 3 : Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.**
```
cd /home/MyFiles/
```
```
sudo touch notes.txt
```
```
ls
```
```
sudo rm -rf notes.txt
```
```
ls
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/683beda1-c1d2-48fd-8d80-55b020c170d5)

**Q 4 : Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.**

```
cd
```
```
ls
```
```
sudo ln document.txt hardlink.txt
```
```
ls
```
```
sudo ln -s document.txt symlink.txt
```
```
ls
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/0321e205-ef8b-4321-8629-236d982b1762)

**Q 5 : In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.**
```
cd MyFiles
```
```
touch ashish.txt abhishek.txt aarti.txt
```
```
ls a*txt
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/0f438da5-bb03-43c5-a9cd-500bdd5a7b25)


**Q 7: Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."**

```
cd /home
```
```
cd MyFiles
```
```
sudo mkdir backup
```
```
cd
```
```
sudo cp /home/MyFiles/Document/* /home/MyFiles/backup/
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/6eca4906-291a-4621-bb34-a72a7e5e2b6a)

**Q 8 :Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.**
```
sudo su
```
```
cd /home/MyFiles/
```
```
touch file_list.txt
```
```
cd Document
```
```
cd ..
```
```
chmod +rwx file_list.txt
```
```
cd Document
```
```
ls > ../file_list.txt
```
```
cd ..
```
```
grep '\.txt$' file_list.txt
```
**Output :**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/18e3bb96-6dec-487a-966b-b4bc65cac0dd)

**Q 9: Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.**
```
cd /home/MyFiles/
```
```

sudo touch my_notes.txt
```
```
ls
```
```
sudo vim my_notes.txt
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/b097a7e6-1cff-43c0-9197-ecd57b52436a)


![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/dfe2a2f0-e375-4f80-a2e3-295d867f24a5)

**Ques 10 :Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.**

```
cd /home/MyFiles/
```
```
sudo su
```
```
current_date=$(date)
```
```
echo "current date : $current_date"
```
```
echo "$current_date" >> my_notes.txt

```

**Output**


![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/5803a8b5-19ae-4362-8d65-dd0b03d6f942)

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/83d672b5-340b-4d6f-a77b-8ade5d1f18d7)


**Ques 12 : Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.**

```
cd /home/MyFiles

```
```
sudo su

```
```
"How are you" >> my_notes.txt
```
```
cat my_notes.txt
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/4dde6569-698f-4d10-9172-094ad1ad43d7)


**Q 13 : List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."**
```
ls /etc | grep 'conf' > conf_files.txt

```
```
vim conf_files.txt

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/f8209353-2637-48ed-bc82-73f7509e28fd)

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/89d1a310-c936-4288-953d-75379877091d)

**Ques 15 : Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.**
```
grep '^users:' /etc/group

```
```
sudo adduser --home /home/john_doe john_doe

```
```
sudo usermod -aG users john_doe
```
```
id john_doe
```	

**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/f1990a10-11d1-4b74-864f-713ba1d9e665)


![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/72b468d1-456f-44bb-9046-c7c7dd9f8336)

**Ques 16 : Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.**
```
sudo usermod -aG users john_doe
```
```
id john_doe
```
```
su - john_doe
```
```
sudo apt update
```
```
exit
```
```
sudo usermod -aG sudo john_doe
```
```
id john_doe
```
```
su - john_doe
```
```
sudo su

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/87a18e19-1126-45bb-9f75-1e5bdbb5dfbf)


**Ques 17 :Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.**

```
sudo chsh -s /bin/bash john_doe
```
```
sudo chage -E $(date -d "+1 month" +"%Y-%m-%d") john_doe

```
**Output**
![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/15efdbd2-c73d-4b4d-a37d-a83c580240c0)

**Ques 18 :Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.**
```
sudo groupadd development_team
```
```
sudo usermod -aG development_team john_doe
```
```
getent group development_team

```
***Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/3dd26ed5-cc90-4ec9-bae5-c547899e89c5)


**Q19. Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.**
```
id john_doe
```
```
sudo deluser john_doe users

```
```
sudo adduser john_doe development_team

```
```
id john_doe

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/402ef2f2-314b-47a8-9710-f95e905a8188)

**Q20. Delete the user account "john_doe" and ensure that their home directory is also removed.**
```
sudo deluser --remove-home john_doe

```
```
id john_doe

```
```
ls /home/john_doe

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/ca93a5d7-28ef-4719-8b35-4a77c0959d2b)


**Q21. Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.**
```
sudo deluser john_doe development_team
```
```
sudo delgroup development_team
```
```
grep development_team /etc/group
```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/9ed62efa-af7a-46f7-b1a6-739904d66868)

**Q22. Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.**
```
sudo chage -M 90 -m 0 -W 7 -I 30 -E -1 $(cut -d: -f1 /etc/passwd)

```
```
sudo sed -i '/^PASS_MAX_DAYS/c\PASS_MAX_DAYS   90' /etc/login.defs

```
```
sudo chage -l john_doe
```
```
grep PASS_MAX_DAYS /etc/login.defs

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/77286fcf-b408-42ed-a7f1-239ffd701692)

**Q23. Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.**
```
sudo passwd -l john_doe

```
```
su - john_doe

```
```
sudo su - john_doe

```
```
sudo passwd -u john_doe

```
```
exit
```
```
sudo passwd -u john_doe

```
```
su - john_doe

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/a0867924-ef00-43fb-b5cb-924784fdf61e)


**Q24. Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.**
```
id john_doe
```

**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/a4c638eb-ba66-4642-b11d-5b0d0f860672)

**Q25. Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.**
```
sudo adduser john_doe

```
```
sudo grep 'john_doe' /etc/passwd

```
```
sudo chage -M 60 john_doe

```
```
sudo chage -l john_doe

```
**Output**

![image](https://github.com/sachinkumarbhati/sachinkumarbhati/assets/158732178/713ed23f-77b3-4780-a30f-02b39113d0ff)


