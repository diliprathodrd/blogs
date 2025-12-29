---
title: "Inside Git: How It Works and the Role of the .git Folder"
datePublished: Mon Dec 29 2025 12:12:50 GMT+0000 (Coordinated Universal Time)
cuid: cmjr4cnmr000102l43nv3eh00
slug: inside-git-how-it-works-and-the-role-of-the-git-folder
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1767010058290/5a739907-3191-4730-a882-6886a84b98e9.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1767010359725/dd9b3912-1b8e-4806-bc35-b2f30c7c341a.png
tags: git, hiteshchoudharylco, piyushgarg, webdevcohort2026

---

In the previous blog, we talked about **why version control exists** and how Git solved the pendrive problem.

Now comes the next natural question:

> *“Okay, I use Git… but what is Git actually doing behind the scenes?”*

This blog answers that question.

No magic.  
No memorizing commands.  
Just a simple mental model of how Git works internally.

## Git Is Not Just Commands

Most beginners learn Git like this:

* `git add`
    
* `git commit`
    
* `git push`
    

But they don’t really know **what happens when they run these commands**.

The truth is:  
👉 Git is just a **content tracker**  
👉 And everything Git does lives inside one folder

That folder is called `.git`.

## The `.git` Folder: Git’s Brain

When you run:

```bash
git init
```

Git creates a hidden folder called `.git`.

This folder is **the heart of your repository**.

If you delete the `.git` folder:

* Your files remain
    
* But Git forgets everything
    
* No history, no commits, no tracking
    

That’s because **Git does not store history in your code files**.  
It stores everything inside `.git`.

Think of it like this:

> Your project folder is the body  
> The `.git` folder is the brain

## What Lives Inside the `.git` Folder (Conceptually)

You don’t need to memorize the internal files, but you *do* need to understand the idea.

Inside `.git`, Git stores:

* Snapshots of your files
    
* Metadata (author, message, time)
    
* Pointers to history
    
* Integrity checks using hashes
    

All of this works using **Git objects**.

## Git Objects: The Core Idea

Git stores data using three main object types:

* **Blob**
    
* **Tree**
    
* **Commit**
    

Let’s understand them without jargon.

## Blob: The File Content

A **blob** represents the **content of a file**.

Not:

* File name
    
* File path
    
* File permissions
    

Only:  
👉 The **actual content**

Important idea:

* If two files have the same content, Git stores **only one blob**
    
* This is why Git is efficient
    

## Tree: The Folder Structure

A **tree** represents a directory.

It contains:

* File names
    
* Folder names
    
* References to blobs and other trees
    

Think of a tree as:

> “This folder contains these files and subfolders”

Trees connect blobs together into a structure.

## Commit: A Snapshot in Time

A **commit** is not a diff.  
It’s a **snapshot** of your project at a specific moment.

A commit contains:

* A reference to a tree (project structure)
    
* Author information
    
* Commit message
    
* A reference to the previous commit
    

This is how Git builds history — **commit by commit**.

## How Git Tracks Changes (The Right Mental Model)

Git does **not** track changes like Word or Google Docs.

Instead, Git:

* Takes snapshots
    
* Links snapshots together
    

Each commit says:

> “Here is what the entire project looks like right now”

Changes are inferred by comparing snapshots.

## What Happens During `git add`

When you run:

```bash
git add file.txt
```

Git does **not** create a commit.

Instead:

* Git takes the content of the file
    
* Converts it into a blob
    
* Stores it inside `.git`
    
* Adds it to a staging area
    

Think of staging as:

> “I’m telling Git: this version of the file is ready”

## What Happens During `git commit`

When you run:

```bash
git commit
```

Git:

1. Takes everything from the staging area
    
2. Builds a tree (folder structure)
    
3. Creates a commit object
    
4. Links it to the previous commit
    

Now Git has a new snapshot in history.

## Why Git Uses Hashes Everywhere

Every Git object (blob, tree, commit) has a **hash**.

That hash is:

* Generated from the content itself
    
* Unique
    
* Immutable
    

Why this matters:

* If content changes → hash changes
    
* If hash matches → content is guaranteed the same
    

This gives Git:

* Data integrity
    
* Safety
    
* Trust in history
    

Git literally knows if something was altered or corrupted.

## The Big Picture Mental Model

Here’s the mental model you should keep:

* `.git` is where everything lives
    
* Git stores **snapshots**, not diffs
    
* Files → blobs
    
* Folders → trees
    
* History → commits
    
* Hashes ensure integrity
    
* Commands are just ways to interact with this system
    

Once this clicks, Git stops being scary.

## Why You Should Care About This

When you understand how Git works internally:

* Merge conflicts make more sense
    
* Reset, checkout, and revert feel logical
    
* You stop memorizing commands blindly
    
* Debugging Git issues becomes easier
    

You start **using Git with confidence**.

## What’s Coming Next

In the next part of this series, we’ll talk about:

* Git vs GitHub (they are NOT the same)
    
* Local repositories vs remote repositories
    
* What actually happens during `git push` and `git pull`
    

## Final Thoughts

Git isn’t magic.

It’s a well-designed system built on:

* Snapshots
    
* Objects
    
* Hashes
    
* History
    

Understand the system, and the commands will follow naturally.

This is how you truly learn Git — from the inside out.