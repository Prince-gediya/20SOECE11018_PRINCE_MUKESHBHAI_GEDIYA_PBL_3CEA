# 20SOECE11018_PRINCE_MUKESHBHAI_GEDIYA_PBL_3CEA

Have you ever annoyed with a lot of unorganized files in your folder?
if yes, then this python script will help you automatically organize the files based on their type.


First of all,we have imported OS and SHUTIL modules in our code.This both are inbuild modules so we don't have to install them.
- import os
- import shutil

second we have to create two variable path and files.path is for taking input from user and files that consist list of files
- path=input('enter your path')
- files=os.listdir(path)

then we have to add loop condition. By for loop condition we can traverse through every file from files. then we split the filename and extension extension of the file.
- for file in files:
-    filename,extension=os.path.splitext(file)

we only need extension name so we remove the dot from through slicing.
-    extension=extension[1:]

the adding if statement.the condition is-if extension dictionary already exist,then we move files to that dictionary.
-    if os.path+'/'+extension):
-         shutil.move(path+'/'+file,path+'/'+extension+'/'+file)

in else statement we make a new dictionary and we move files into it.
-    else:
-         os.makedirs(path+'/'+extension)
-         shutil.move(path+'/'+file,path+'/'+extension+'/'+file)
