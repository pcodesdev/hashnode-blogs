---
title: "How to Push Files Over 100MB to GitHub: A Step-by-Step Guide with Git Large File Storage (LFS)"
seoTitle: "Pushing Large Files to Github with LFS"
seoDescription: "Learn how to use Git LFS to push large files to GitHub with my comprehensive guide. Say goodbye to the 100MB limit!"
datePublished: Fri Apr 21 2023 16:28:36 GMT+0000 (Coordinated Universal Time)
cuid: clgqrn7cu000309ml01daamx3
slug: how-to-push-files-over-100mb-to-github-a-step-by-step-guide-with-git-large-file-storage-lfs
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/a4X1cdC1QAc/upload/9a0af1111247ac3f72a31a7aaabd076a.jpeg
tags: github, git, codenewbies, github-actions-1, gitcommands

---

# Git Large File Storage (LFS)

Git Large File Storage (LFS) is a tool that allows large files to be stored outside of a Git repository while still being version controlled. Here are the step-by-step instructions to use Git LFS on the three major operating systems:

## Windows:

1. Download and install Git from [**https://git-scm.com/download/win**](https://git-scm.com/download/win).
    
2. Download and install Git LFS from [**https://git-lfs.github.com/**](https://git-lfs.github.com/).
    
3. Open Git Bash or Git CMD and navigate to the repository directory.
    
4. Initialize Git LFS by typing "<mark>git lfs install</mark>" and press Enter.
    
5. Add the files you want to track with Git LFS by typing "<mark>git lfs track [filename]</mark>" and press Enter.
    
6. Commit and push the changes to the repository using Git as you would normally.
    

## MacOS:

1. Download and install Git from [**https://git-scm.com/download/mac**](https://git-scm.com/download/mac).
    
2. Download and install Git LFS from [**https://git-lfs.github.com/**](https://git-lfs.github.com/).
    
3. Open Terminal and navigate to the repository directory.
    
4. Initialize Git LFS by typing "<mark>git lfs install</mark>" and press Enter.
    
5. Add the files you want to track with Git LFS by typing "<mark>git lfs track [filename]</mark>" and press Enter.
    
6. Commit and push the changes to the repository using Git as you would normally.
    

## Linux:

1. Install Git by running the command "sudo apt-get install git" on Ubuntu or Debian or by downloading from [**https://git-scm.com/download/linux**](https://git-scm.com/download/linux).
    
2. Download and install Git LFS from [**https://git-lfs.github.com/**](https://git-lfs.github.com/).
    
3. Open Terminal and navigate to the repository directory.
    
4. Initialize Git LFS by typing "<mark>git lfs install</mark>" and press Enter.
    
5. Add the files you want to track with Git LFS by typing "<mark>git lfs track [filename]</mark>" and press Enter.
    
6. Commit and push the changes to the repository using Git as you would normally.
    

It is important to note that once Git LFS is installed and initialized, any large files added to the repository will be automatically tracked by Git LFS. To learn more about Git LFS, visit their website at [**https://git-lfs.github.com/**](https://git-lfs.github.com/).

# Conclusion

In conclusion, pushing large files to GitHub can be a challenge, especially if the file exceeds 100 MB. However, using Git Large File Storage (Git LFS) can make the process easier and more efficient. By following the step-by-step process outlined for Windows, Mac, and Linux operating systems, users can successfully push large files to GitHub without any issues. Git LFS is a powerful tool for managing large files in version control, and it's definitely worth exploring for any project that involves working with large files.