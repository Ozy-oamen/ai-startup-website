# Git Collaboration: Tom's Workflow Documentation

## Project Context
A team is developing a website for an AI startup using Git for version control. Two developers (Tom and Jerry) need to modify the same `index.html` file simultaneously:
- **Tom's Task**: Update the navigation bar
- **Jerry's Task**: Add contact information to the footer

## Prerequisites
- Git installed locally
- Access to central repository (GitHub)
- Clone of the project repository



## Tom's Step-by-Step Workflow
```bash
## Before i start there will be need for some Git configuration of user credentials
```
- The commands seen on the screenshot below shows a successful configuration of the users credentials.
![img1ii](./Img-git/img1ii.png)
### 1. Fork the project's repository
- Since Tom was only sent the projects URL, his first step was to fork the repository to enable him contribute to the project.

![img1](./Img-git/img1.%20Fork.png)

### 2. Initialize Workspace
- Using bash CLI clone the repository and cd into the project directory.
```bash
# This bash command will clone the repository (since have already forked it into Tom's repository)

git clone https://github.com/Ozy-oamen/ai-startup-website.git 
```
![img2](./Img-git/img3.%20git%20clone.png)

- Start from the origin main branch and update Tom's copy of the project with the commands below.
```bash
# The commands below will Ensure Tom start from the origin main branch and have the lastest version of the project.

git checkout main
git pull origin main
```
![img3b](./Img-git/Img3b-git%20pull.png)

### 3. Create Feature Branch

- Creating a feature branch will enable Tom add the navigation bar feature with out interferring with the man branch.

```bash
# This command will create a new feature branch "update-navigation".

git checkout -b update-navigation
```
![img4](./Img-git/img4.%20git%20checkout.png)

### 4. Make Changes
- Open index.html in your editor

- Modify the navigation bar HTML

- Save the file

![img5](./Img-git/img5.png)

### 5. Add changes

- Use the command "git status" and "git add index.html" to check the status of the file, as well as add the file to the staging area.

```bash
# The commands below will do the following to the index.html file.

# Check status 
git status

# Stage Changes
git add index.html
```
![img6](./Img-git/img6.png)

### 6. Commit changes

- Use the "git status" command to confirm the index.html file is in the staging area and ready to be commited.
- commit the index.html file for it to be ready to be pushed.

```bash
# Confirm changes is staged
git status

# Commit with descriptive message
git commit -m "feat: Update main navigation with new menu structure"
```
![img7](./Img-git/img7.png)

### 7. Push to Remote

```bash
# This bash command will push all the changes to Tom's github repository.
git push -u origin update-navigation
```
![img8](./Img-git/img8.png)

### 8. Create Pull Request
- Tom goes to his GitHub repository; He  notices there is a prompt to compare and pull request.
- Tom Clicks on the prompt "Compare and pull request" to request for a new pull request.
- Add PR title: "Navigation Update"
- Add description explaining changes
- Click "Create Pull Request" and Request review from a teammate.

![img9](./Img-git/img9.png) 

![img10](./Img-git/img10.png)


### 7. After PR Approval

- Once approved by the team after a pull request is recieved and reviewed by a team mate

- The teammate now merges the PR

- Changes are now in the main branch

- Tom can delete his local branch:

![img-main](./Img-git/img-main.png)

![img-main2](./Img-git/img-main2.png)

![img-main3](./Img-git/img-main3.png)

![img-main4](./Img-git/img-main4.png)







## Jerry's Step-by-Step Workflow

### 1. Switch Back to the Main Branch
```bash
## This command switches your current directory back to the main branch.
git chechout main 
``` 
### 2. Initialize Workspace
- Using bash CLI  to clone  the repository and cd into the project directory.
```bash
# This bash command will clone the repository.

git clone https://github.com/wilfredoamen/ai-startup-website.git
```
![img1b](./Img-git/./img1b.png)

- Since we have already switched to the origin main branch, update Jerry's copy of the project with the commands below.
```bash
# The commands below will ensure Jerry starts from the lastest version of the project.

git pull origin update-navigation
```
![img1a](./Img-git/img1a.png)

### 3. Create a new branch for Jerry's contribution

```bash
# This will create a now branch for jerry to make his changes, keeping them separate from the main project until they are ready to be merged.

git chechout -b add-contact-info
```
![img2a](./Img-git/Img2a.png)

### 4. Open VScode to update contact-informations

- Jerry uses VScode to add the contact information to the index.html file.

![img3a](./Img-git/img3a.png)

### 5. Stage the changes made by Jerry

- The command below will stage the changes made on on the index.html file and preparing the file for it to be commited. 

```bash
git add index.html
```
![img4a](./Img-git/img4a.png)

### 6. Commit Jerry's changes

- The command below will save jerry;s changes to the branch history,with a message describing the exact changes made on the index.html file. 

```bash
git commit -m "Added contact information"

```

![img5a](./Img-git/img5a.png)

### 7. Push Jerry's branch to the github repo.

- The command below uploads Jerry's branch to the github repository, for someone to review and merge  changes  made on the index.html file to the main.

```bash
git push origin add-contact-info

```
![img6a](./Img-git/img6a.png)


### 8. Create Pull Request
- Jerry goes to his GitHub repository; He  notices there is a prompt to compare and pull request.
- Jerry Clicks on the prompt "Compare and pull request" to request for a new pull request.
- Add PR title: "Add contact info"
- Add description explaining changes
- Click "Create Pull Request" and Request review from a teammate.

![img7a](./Img-git/img7a.png)


![img8a](./Img-git/img8a.png)




### 9. After PR Approval

- Once approved by the team after a pull request is recieved and reviewed by a team mate

- The teammate now merges the PR

- Changes are now in the main branch

- Jerry can delete his local branch:

![img9a](./Img-git/img9a.png)

![img10b](./Img-git/img10b.png)

![img10a](./Img-git/img10a.png)


