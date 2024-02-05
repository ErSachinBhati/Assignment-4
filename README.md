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

**Q 6: Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.**

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


