# C++ Version Control System

This project is a simple, lightweight version control system implemented in C++. It mimics some of the basic functionalities of Git, such as initializing a repository, adding files to a staging area, committing changes, viewing the commit log, and reverting to previous commits.

## Features

*   **Initialize Repository**: Create a new version control repository.
*   **Stage Files**: Add files to the staging area for the next commit.
*   **Commit Changes**: Save the staged changes as a new commit.
*   **View Commit Log**: See the history of all commits.
*   **Revert Commits**: Roll back the project to a previous state.

## Getting Started

### Prerequisites

To compile and run this project, you will need a C++ compiler that supports C++17 (for the `<filesystem>` library).

### Compilation

To compile the project, you can use g++:

```bash
g++ -std=c++17 main.cpp -o git-clone
```

This will create an executable file named `git-clone`.

## Usage

Here are the available commands:

*   `git-clone init`
    *   Initializes a new repository in the current directory. This creates a `.git` directory with `staging_area` and `commits` subdirectories.

*   `git-clone add <file1> [file2] ...`
    *   Adds one or more files to the staging area. You can also use `.` to add all files in the current directory.

*   `git-clone commit -m "Your commit message"`
    *   Creates a new commit with the files from the staging area and a commit message.

*   `git-clone log`
    *   Displays the history of all commits, including the commit ID, message, and timestamp.

*   `git-clone revert <commit_hash>`
    *   Reverts the project to the state of a specific commit. You can also use `HEAD` to revert to the latest commit.

## Project Structure

The project is organized into three main C++ files:

*   `main.cpp`: The entry point of the application. It parses command-line arguments and calls the appropriate functions.
*   `gitClass.cpp`: Contains the `gitClass` which implements the core logic for the version control system's commands.
*   `commitNodeList.cpp`: Implements a linked list to manage the commit history. Each node in the list represents a single commit.
