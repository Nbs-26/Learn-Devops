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
