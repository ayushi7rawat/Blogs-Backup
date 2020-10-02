## GitHub CLI 1.0: All you need to know

Earlier this year, GitHub announced the beta of GitHub CLI and GitHub CLI 1.0 is now available.

GitHub CLI basically brings GitHub to your terminal. With GitHub CLI, developers can check the status of GitHub issues and pull requests, search for a specific issue or PR, create/fork a repo, or create new issues and pull requests right from the command line.

It reduces context switching, helps you focus, and enables you to more easily script and create your own workflows. 

What will be covered in this blog post:

1. What Is GitHub CLI
2. How to download and Authenticate 
3. Managing GitHub Repositories using GitHub CLI 
4. Working with Pull Requests using GitHub CLI
5. Managing GitHub Issues using GitHub CLI
6. Working with GitHub gist using GitHub CLI 
7. GitHub alias using GitHub CLI



# **What Is GitHub CLI?**
Let's start with a brief overview of GitHub CLI.  GitHub CLI can be best described as “GitHub from the command line.”

With GitHub CLI 1.0, you can:

-  Run your entire GitHub workflow from the terminal, from issues through releases

-  Call the GitHub API to script nearly any action, and set a custom alias for any command

-  Connect to GitHub Enterprise Server in addition to GitHub.com

`gh` is GitHub on the command line. It brings pull requests, issues, and other GitHub concepts to the terminal next to where you are already working with git and your code.

## **How to download it?**
To install GitHub CLI on your machine, you can refer to the installation guide found on GitHub. To download click the [Link](https://cli.github.com/)
Click the link to navigate to the [guide](https://github.com/cli/cli#installation-and-upgrading)

GitHub CLI is available across all platforms, MacOS, Windows and various Linux.

## **Authentication**
After a successful installation, you need to authenticate your Github account.

To authenticate your account you need to use the following command. 
```
gh auth login
```
Follow the series of steps to complete your authentication process. After authentication, you can use the GitHub CLI.









# **Managing GitHub Repositories using GitHub CLI **
`gh repo` command is used to create, clone, fork, and view repositories.

### **1. View GitHub Repositories**

Display the description and the README of a GitHub repository. With no argument, the repository for the current directory is displayed.

```
gh repo view [<repository>] [flags]
``` 

**Open a repository in the browser**

You can open the repository in a web browser with `-w, --web ` commands instead.

### **2. Create GitHub Repositories**
To create a new GitHub repository use the following command.

```
gh repo create [<name>] [flags]
``` 
for example: create a repository with a specific name

```
$ gh repo create demo-repository
``` 
### **3. Fork GitHub Repositories**
Lets fork of a repository with GitHub CLI.

If you don't provide any argument, creates a fork of the current repository. Otherwise, forks the specified repository.
```
gh repo fork [<repository>] [flags]
```







# **Working with Pull Requests using GitHub CLI**

Let’s explore the use of GitHub CLI for managing pull requests.
 
### **1. List Pull Requests**
```
gh pr list
``` 
If we want to list out ALL of the pull requests, both open and closed, we could use the “state” flag

```
gh pr list --state "all"
gh pr list -s "all"
```

when listing out all PRs, instead of using this full command

```
gh pr list --label "labelname"

``` 

### **2. Check Pull Request Status**
If you wish to check the status the PRs you created earlier, you can use the `status command` to list them at the terminal

```
gh pr status
``` 
This will give you a list of PRs that are assigned to you, mentioning you, or that were opened by you.

If you wish to check whether a PR is closed or not, use the following command.

```
gh pr list --state "closed"
gh pr list -s "closed"
``` 
If you wish to list out all of our open bug fix PRs,  you could check by listing all the open PRs again

You could also filter by the defining label-name in the GitHub repo.

### **3. View Pull Request**
You can open the PR from the command line using the view command.

```
gh pr view [<number> | <url> | <branch>] [flags]
``` 
It will open the pull request in a web browser where you can then assign it to yourself, review it, etc.

### **4. Create Pull Request**
You can use the following command to create a new pull request directly from the command line.

```
gh pr create --title "Pull request title" --body "Pull request body" 
``` 

You’ll have an option to submit the PR, you can open it the browser, or cancel.

If you prefer to create your PR from the web, you could use the following command to open up a browser window.

```
gh pr create --web
``` 

### **5. Checkout Pull Request**

You can checkout a Pull Request in GitHub CLI using the following command.

```
gh pr checkout {<number> | <url> | <branch>} [flags]
``` 








# **Managing GitHub Issues using GitHub CLI **
### **1. List Issues With GitHub CLI**
```
gh issue list
```

If we want to list out ALL of the issues we could use the `state` flag
```
gh issue list --state "all"
gh issue list -s "all"
```

### **2. Checking Issue Status With GitHub CLI**
You can use the following command to list them at the terminal.

```
gh issue status
``` 
This will give you a list of issues that are assigned to you, mentioning you, or that were opened by you.

In case you cannot find the issue you’re looking for, so let's check if its closed.

```
gh issue list --state "closed"
gh issue list -s "closed"
``` 

If you wish to filter out you can filter by the “labelname” label defined in your GitHub repo
```
gh issue list --label "labelname"
gh issue list -l "labelname"
``` 

### **3. Viewing Issues With GitHub CLI**
You can open the issue from the command line using the following command.

```
gh issue view {<number> | <url>} [flags]
``` 
for example:

```
gh issue view "10" 
```

### **4. Creating Issues With GitHub CLI**
You can create an issue with the help of the following command.

```
gh issue create --title "Issue title" --body "Issue body"
``` 
At the end you’ll have an option to submit the issue, open it the browser, or cancel.

If you still prefer to create your issue from the web, you could use the following command


```
gh issue create --web
``` 







# **Working with GitHub gist using GitHub CLI **

### **1. List gist with GitHub CLI**

You can list your gists with GitHub CLI using the following command.
```
gh gist list [flags]
```

### **2. View gist with GitHub CLI**
You can view your gists with GitHub CLI using the following command.
```
gh gist view {<gist id> | <gist url>} [flags]
```
### **3. Create gist with GitHub CLI**
Create a new GitHub gist with given contents. Gists can be created from one or multiple files. Alternatively, pass “-“ as file name to read from standard input.

By default, gists are private; use ‘–public’ to make publicly listed ones.

```
gh gist create [<filename>... | -] [flags]
```

# **Working with GitHub alias using GitHub CLI **
You can print out all of the aliases `gh` is configured to use using the following command.
```
gh alias list [flags]
```


I hope this helped you. 
You can connect with me on [Twitter](https://twitter.com/ayushi7rawat)


Also, have look at my other blog:

[Python 3.9: All you need to know about](https://ayushi7rawat.hashnode.dev/python-39-all-you-need-to-know)




Resources:
- https://github.blog/2020-09-17-github-cli-1-0-is-now-available/
- https://cli.github.com/manual/
- https://github.com/cli/cli