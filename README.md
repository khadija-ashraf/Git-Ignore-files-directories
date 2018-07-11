# Git-Ignore Files/Directories in Windows

While adding files into git repository we can follow two approaches  to ignore certain files/directories.

- Adding ".gitignore" file
- Editing "exclude" file**

### Adding ".gitignore" file
---
 ##### 1. Create a file named '.gitignore'
  - Windows will give below error if we want to create a file name like '.gitignore'.
  ![Image of Yaktocat](https://i.stack.imgur.com/IJxts.png)
  - To avoid that, create a file with an extra dot at the end of the file name, that is **'.gitignore.'** and you will see Windows will automatically remove the last dot. A file will be created with name **.gitignore**
 #### 2. Keep the '.gitignore' file in the root dictory of the repository.
  - Do NOT keep the **.gitignore** file inside **.git** folder. Keep it beside .git. 
  - For example
    ```sh
    $ ls 
    .git
    .gitignore
    data
    tracker.m
    README.md
    ```   

 #### 3. Add the files and directory into **.gitignore** file with any text editor.
There is no git command to add or edit the the .gitignore file. We can do it with any text editor.
  - To avoid all files inside **data** folder from above given directory structure of the repository, we need to add blow line inside **.gitignore** file.
    ```sh
    data/*
    ```   
    Or, suppose to avoid any **.jpg** file we can add another line below it.
    ```sh
    data/*
    *.jpg
    ```   
### Editing "exclude" file
---
After we execute **$git init** command a hidden folder named **.git** is created inside our local repository folder. This .git folder has a folder named **info**. Inside **info** folder there is a file named **exclude**. We can add the same rules that we have added in **.gitignore** file. The impact is exactly same. This way we can avoid steps of creating and using **.gitignore** file.
