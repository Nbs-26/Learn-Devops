A Bare-Git-Repository is a repository/folder with **only** Git's internal contents(**.git file**) and **no working directory** (no checked-out files).
👉 It is mainly used as a central/shared repository for collaboration (for example, on a server).

| Feature           | Normal Git repo              | Bare Git repo                           |
| ----------------- | ---------------------------- | --------------------------------------- |
| Working directory | ✅ Yes (source files present) | ❌ No                                    |
| `.git` folder     | ✅ Hidden directory           | ❌ Not present (repo itself *is* `.git`) |
| Can edit files    | ✅ Yes                        | ❌ No                                    |
| Used for          | Development                  | Central / remote repo                   |
| `git push` target | ❌ Not recommended            | ✅ Ideal                                 |

How to initialize a bare Git repository?

Method 1: Initialize directly (most common)
git init --bare project.git

This creates a directory:

project.git/
├── HEAD
├── config
├── objects/
├── refs/
├── hooks/

⚠️ Notice: no source code files

**Can I use my system similar to Github allowing developers to contribute the code to repo in my system?**
Answer : Yes, although I cant reproduce the same UI as Github currently, the functionality can be replicated and will show you how.

**Method-1**(Simplest): Push via File System Path (LAN / Shared Folder)
Step-1 : Create a Bare Git Repository.
Command : git init --bare <repo-name>.git
<img width="737" height="278" alt="image" src="https://github.com/user-attachments/assets/b676bea0-3ee8-4b8b-b818-91612bba16de" />
Note : .git contents are only present.(No working directory). You can't add files here


