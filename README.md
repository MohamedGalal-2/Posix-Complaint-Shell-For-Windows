# Posix-Compliant-Shell-For-Windows

This repository hosts a POSIX-compliant shell implementation tailored for Windows environments. The shell aims to provide a familiar command-line interface while bridging the gap between POSIX standards and Windows-specific limitations.

![Header](https://github.com/MohamedGalal-2/Posix-Complaint-Shell/blob/main/asset.jpg)

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Commands](#commands)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

### Introduction
While Windows offers its command-line interface, it lacks some features and commands present in POSIX-compliant systems like Unix and Linux. This shell project aims to provide those missing functionalities in a Windows environment.

### Installation
To install the shell, clone this repository using the following command:

```bash
git clone https://github.com/MohamedGalal-2/Posix-Compliant-Shell.git
```

Navigate to the project directory and compile the source code:

```bash
cd Posix-Compliant-Shell
gcc -o posix_shell main.c shell.c builtIns.c colors.c command_handling.c parser.c
```

### Usage
Start the shell by running the compiled executable:

```bash
./posix_shell
```

You can then enter commands as you would in a standard shell. Type `exit` to quit the shell.

### Commands
This shell provides several built-in commands:

- **cd**: Changes the current directory. Supports `~` as a home directory shortcut.
  ```sh
  cd ~
  cd ~/Documents
  ```

- **cat**: Concatenates and displays the contents of files.
  ```sh
  cat file1.txt file2.txt
  ```

- **ls**: Lists the files in the current directory. Supports options `[-a]`, `[-f]`, and `[-af]`, as well as specifying a path.
  ```sh
  ls
  ls -a
  ls /path/to/directory
  ```

- **./[file]**: Executes a file in the current directory.
  ```sh
  ./script.sh
  ```

- **type**: Displays if a command is a built-in command or an external command.
  ```sh
  type ls
  ```

- **echo**: Prints a string to the terminal or writes a string into a file using the `>` symbol.
  ```sh
  echo "Hello, World!"
  echo "Hello, World!" > output.txt
  ```

- **pwd**: Displays the current working directory.
  ```sh
  pwd
  ```

- **help**: Lists the available commands.
  ```sh
  help
  ```

- **exit [n]**: Exits the shell with an optional exit status.
  ```sh
  exit
  exit 0
  ```

### Examples
Explore some commands that are traditionally associated with POSIX systems but may not be supported natively in Windows:

```sh
# Running a simple command
ls -l

# Using input and output redirection
cat < input.txt > output.txt

# Piping commands
ls -l | grep ".c"

# Setting and using environment variables
export MY_VAR="Hello"
echo $MY_VAR

# Running a command in the background
sleep 60 &
```

### Contributing
Contributions are welcome! If you have ideas or improvements, please fork this repository, make your changes, and submit a pull request.

### License
This repository is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
