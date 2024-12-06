

|  SCHOOL OF INFORMATION AND TECHNOLOGY |  |  |
| ----- | :---- | :---: |
| NAME: Villena, Aeron Jeff A. | DATE PERFORMED: 11/21/24 |   |
| Section: IDC2 | DATE SUBMITTED: 11/26/24 |  |

1. # SYSADM1 – Git Basics

Answer the following research questions about Git, GitLab desktop and GitHub.

1. What is Git, and why is it important in software development?

- Git is a free, open-source version control system that helps software developers collaborate by tracking changes in code during development. It allows multiple developers to work on the same project simultaneously without conflicts, manage versions easily, and revert to earlier versions when needed. This makes Git essential for maintaining a project's integrity and history, especially in large-scale development where frequent changes are common.


2. How does Git track changes in a project?

- Git tracks changes by creating snapshots of the project whenever a change is committed. Each snapshot captures the current state of the files along with metadata like the author and timestamp. These snapshots are connected through unique identifiers called commit hashes, enabling developers to easily revert to any previous state when needed.


3. What is the difference between a local repository and a remote repository in Git?

   A local repository is stored on a developer's machine, allowing them to make changes, commit updates, and manage versions independently. A remote repository, hosted on a server like GitHub or GitLab, acts as a centralized hub for collaboration. Developers can push changes from their local repository to the remote one to share updates or pull updates from the remote repository to stay synchronized with others.

   

4. What are the basic Git commands? 

- **git init** \= Initializes a new Git repository

- **git clone** \[*repository-url*\] \= Creates a local copy of a remote repository

- **git add** \[*file*\] \= Stages changes for the next commit

- **git commit \-m** "*message*" \= Commits staged changes with a descriptive message

- **git status** \= Displays the status of the working directory and staging area

- **git push** \= Uploads local commits to a remote repository

- **git pull** \= Fetches and merges changes from a remote repository into the local branch


5. How do you check the status of a Git repository? 

- The ***git status*** command shows the status of your working directory and staging area, including which files are staged for commit, modified but not yet staged, or untracked by Git.


6. What is the purpose of branches in Git, and how do you create and switch between them?

- Branches in Git allow developers to work on different features or fixes in isolation from each other. This enables multiple lines of development to occur simultaneously without interfering with the main codebase.

  These are the following commands and uses:

- **git branch** \[*branch-name*\] \= To create a new branch

- **git checkout** \[*branch-name*\] \= To switch to an existing branch

- **git checkout \-b** \[*branch-name*\] \= To create and switch to a new branch in one step


7. What are GitLab Desktop and GitHub, and how are they different from Git?

- GitLab Desktop and GitHub are platforms that provide hosting for Git repositories along with additional features like issue tracking, project management tools, and collaborative workflows. They enhance the capabilities of Git by offering user-friendly interfaces for managing repositories online. While Git is the underlying version control system that tracks changes locally and remotely, these platforms provide tools for collaboration and project management on top of that functionality


8. How do you connect a local Git repository to a GitLab or GitHub repository?

- The command, ***git remote add origin** \[repository-url\],* sets up a link between your local repository (referred to as "origin") and the specified remote repository URL, connecting the local Git repository to a remote repository on GitLab or GitHub.

9. What are the steps to collaborate with others using GitLab or GitHub?	

- To collaborate using GitLab or GitHub, follow these steps:

  1. **Clone or Fork**: First, clone an existing repository or fork it if you want your copy.

  2. **Create Branches**: Second, create branches for new features or fixes.

  3. **Make Changes**: Third, make your changes locally and commit them.

  4. **Push Changes**: Fourth, push your branch to the remote repository.

  5. **Open Pull Request**: Fifth, open a pull request (or merge request) for review by collaborators.

  6. **Review & Merge**: Six/Lastly, collaborators/owners will review your changes; once approved, merge them into the main branch. 

10. How do you resolve merge conflicts in Git?

- To resolve merge conflicts in Git:

1. Identify conflicting files using ***git status*** command.

2. Open each conflicting file; look for conflict markers (e.g., \<\<\<\<\<\<\< HEAD).

3. Edit the file to resolve conflicts manually.

4. After resolving all conflicts, stage the resolved files using ***git add*** command.

5. Complete the merge by committing with the ***git commit***.

   

11. What is a pull request, and why is it used in GitHub?

- A pull request (PR) is a way to propose merging code changes from one branch into another on platforms like GitHub. It enables team members to review, discuss, and provide feedback on the changes before they are integrated into the main codebase, promoting quality control and collaborative development.

12. What are some best practices for writing commit messages?

- When writing commit messages, it is essential to follow best practices to ensure clarity and consistency in project history. One key guideline is to use the imperative mood, such as "Fix bug" instead of "Fixed bug," conveying actions clearly and directly. Commit messages should be concise yet descriptive, ideally limited to around 50 characters for the summary line, allowing for a quick understanding of the change's purpose. If additional context is necessary, it can be provided in the body of the message, with lines wrapped at 72 characters for readability. Furthermore, referencing relevant issues or tickets enhances traceability and helps team members understand the rationale behind changes. Adhering to these practices not only maintains clarity in the project's history but also facilitates easier comprehension of changes over time, ultimately improving collaboration among developers.

References:

Forage. (2024). What Is Git? Definition and How to Use It. [https://www.theforage.com/blog/skills/what-is-git](https://www.theforage.com/blog/skills/what-is-git)

Git SCM. (2020). Git Basics \- Recording Changes to the Repository. [https://git-scm.com/book/ms/v2/Git-Basics-Recording-Changes-to-the-Repository](https://git-scm.com/book/ms/v2/Git-Basics-Recording-Changes-to-the-Repository)

Turing School of Software & Design. (n.d.). Git Review \- remotes/locals and forking/cloning. [https://frontend.turing.edu/lessons/module-2/git-forking-vs-cloning.html](https://frontend.turing.edu/lessons/module-2/git-forking-vs-cloning.html)

