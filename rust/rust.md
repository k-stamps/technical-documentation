## Getting Started with Rust

Rust has quickly grown in popularity with developers. It includes features such as a rich type system, more specificity in its ownership model, and a compiler that provides useful error messages. Here are installation steps. If you already have WSL using Ubuntu, then skip step 1.

Note: Rust has a playground environment online, where you can try it out before installing it on your own computer. https://play.rust-lang.org/

### 1. Install Windows Subsystem for Linux (WSL)

Open Windows PowerShell as administrator and run:
```
wsl --install
```
This installs Ubuntu by default.
If prompted, add a Unix username and password of your choosing.
Restart the computer.

### 2. Install Rust with Cargo

Search Windows for Ubuntu and pin it to the taskbar for quick access.
Open the Ubuntu terminal.
Install rust using the wsl command on the Rust install page (reference: https://www.rust-lang.org/tools/install)
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### 3. Explore features in the PowerShell terminal

Once Rust is installed, start a new Ubuntu terminal window (you can close the old one)
To see the options for cargo, the Rust package manager, run:
```
$ cargo 
```

To see information about the Rust compiler, run:
```
$ rustc
```

### 4. Setup VS Code to use WSL and open in Ubuntu:

Open Visual Studio (VS Code).
To be able to run Rust files inside the VS Code terminal window, install the WSL extension:
Open the Extensions panel in the sidebar and search for “WSL.”
Select WSL and click Install.
Close VS Code.

In Windows PowerShell, enter this command:
```
> wsl
```
It should return this message: 
```
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.
```
To open VS Code in Ubuntu, enter this command:
```
$ code .
```

This will open VS Code using Ubuntu. To confirm this, look in the bottom left corner of VS Code for a message that says:
```
“WSL: Ubuntu”
```

In the top bar, select Terminal
See that the terminal starts with the Ubuntu $ prompt.

To confirm that it is connected, enter this command:
```
$ cargo --version
```
It should return the version of cargo you have

To confirm that Rust is installed, enter this command:
```
$ rustc --version
```
It should return the version of rust you have

### 5. Set up a projects folder:

Create your folder for your projects in Ubuntu:
Cntrl + shift + p
Select “show local” to open windows explorer
Type in the path field:
```
\\wsl$
```
In Ubuntu, go into the home/[your username] folder
Create your projects folder there.
Once inside your projects folder, enter this command:
```
$ ls
```
And confirm that shows the contents of your project. It may be empty but you can test it by adding a folder, confirming, then deleting it.

### 6. Install C build tools to use the compiler

Run each of these two commands in the terminal:
```
$ sudo apt update
$ sudo apt install build-essential
```

### 7. Compile and run your first file
Create a new text file and save it as first.rs (the rs is the rust file extension)
Add this code in the first.rs file:
```
fn main(){
    println!("Hello world");
}
```
In the terminal:
$ rustc first.rs
This rustc command compiles the code. You will see a new file created called first in your project folder.
```
$ ./first
```
This runs the compiled file. See that it prints your message “Hello world” in the terminal.

Setup is complete and you can start learning Rust!

Full Rust documentation: 
https://doc.rust-lang.org/book/
