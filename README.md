# Tooling

How to Download & Install MongoDB on Windows.

## Getting Started

These instructions will get you a copy of mongodb up and running on your local machine for development and testing purposes.

### Step 1 — Download the MongoDB MSI Installer Package
```
Download the current version of MongoDB. Make sure you select MSI as the package you want to download.
```

### Step 2 — Install MongoDB with the Installation Wizard
* A. Make sure you are logged in as a user with Admin privileges. Then navigate to your downloads folder and double click on the .msi package you just downloaded. This will launch the installation wizard.
* B. Click Next to start installation.
* C. Accept the licence agreement then click Next.
* D. Select the Complete setup.
* E. Select “Run service as Network Service user” and make a note of the data directory, you’ll need this later.
* F. Deselect (Mongo Compass) and click Next.
* G. Click Install to begin installation.
* H. Hit Finish to complete installation.


### Step 3— Create the Data Folders to Store our Databases
* A. Navigate to the C Drive on your computer using Explorer and create a new folder called _**data**_.
* B. Inside the data folder you just created, create another folder called _**db**_.


### Step 4 — Setup Alias Shortcuts for Mongo and Mongod
Once installation is complete, we’ll need to set up MongoDB on the local system.
* A. Open up your Git Bash terminal.
* B. Change directory to your home directory with the following command:
```
cd ~
```
* C. Here, you’re going to create a file called _**.bash_profile**_ by using the following command:
```
touch .bash_profile
```
* D. Open the newly created _**.bash_profile**_ with vim using the following command:
```
vim .bash_profile
```
* E. In vim, hit the _**I**_ key on the keyboard to enter insert mode.

* F. In your explorer go to C → Program Files → MongoDB → Server
Now you should see the version of your MongoDB.

* G. Paste in the following code into vim, make sure your replace the 4.4 with your version that you see in explorer
```
alias mongod="/c/Program\ files/MongoDB/Server/4.4/bin/mongod.exe"
alias mongo="/c/Program\ Files/MongoDB/Server/4.4/bin/mongo.exe"
```
* H. Hit the _**Esc**_ (Escape) key on your keyboard to exit the insert mode. Then type
```
:wq!
```
to save and exit Vim.

### Step 5 — Verify That Setup was Successful
* A. Close down the current Hyper terminal and quit the application.
* B. Re-launch Git Bash terminal.
* C. Type the following commands into the terminal:
```
mongo --version
```
Once you’ve hit enter, you should see something like this:
```
$ mongo --version
MongoDB shell version v4.4.0
Build Info: {
    "version": "4.4.0",
    "gitVersion": "{hash}",
    "modules": [],
    "allocator": "tcmalloc",
    "environment": {
        "distmod": "windows",
        "distarch": "x86_64",
        "target_arch": "x86_64"
    }
}
```

This means that you have successfully installed and setup MongoDB on your local system!
If you see something that looks like bash mongo command not found, then make sure you check back at all the steps above and follow it step-by-step making sure there are no typos and you haven’t missed any of the steps.

## Bookmarks

* [MongoDB](https://www.mongodb.com/try/download/community) - Document-based, distributed database.
* [Robo 3T (formerly Robomongo)](https://robomongo.org/download) - MongoDB Database Management IDE.
* [Postman](https://www.postman.com/downloads/) - Test calls to APIs.
