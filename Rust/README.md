# Rust!


- General language programming language (Rust is a NEW systems programming language)
	* It seems that Rust really focuses on preserving memory (It looks to pick up where C++ left off and didnt do)
	* It aims to be secure code -- To help 
	* It’s very difficult to write multithreaded code, which is the only way to exploit the abilities of modern machines.
	* Rust is a safe, concurrent language with the performance of C and C++
	- multithreaded code: multithreading specifically refers to the concurrent execution of more than one sequential set(thread) of instructions
		* It can also be referred to as parallel programming
			- paralle programming is the process of using a set of resources to solve a problem in less time dividing the work
		* These threadss could run on a single prcocessor
		
# Understanding Cargo
*An example for of cargo can be found in this directory as "Hello_cargo"*

*Current cargo version is 1.59.0*

- Cargo is Rusts building system and package manager

- Cargo is a useful tool to manage Rust projects and also handle a lot of tasks such as:
	+ Building code
	+ downloading libraries your code depends on
	+ Building libraries
			- libraries your code needs are called "dependancies"

- Cargo comes installed with Rust
  
- to create cargo -- run the following in your terminal:
	+ $ cargo new Hello_cargo 

- Within our directory we will see a new directory titled "Hello_cargo". Go into the new directory, youll see that two files have generated in it
		* Cargo.toml
		* SRC (This directory contains a main.rs file)
		
 - This has also initialized a new Git repo along with a .gitignore file
 - Git files wont be generated if you run new cargo within an existing Git repo
 
 - First we will open our Cargo.toml (.toml = Tom's Obvious, Minimal Labuage)
 	+ .Toml is the format, which is Cargo's configuration format
  - What you will see in .toml is the following

		[package]
		name = "hello_cargo"
		version = "0.1.0"
		edition = "2021"
		
		[dependencies]  	

	
	- The first line [package] -- This section heading indicates that the following statements are configuring  a package
	- the next three lines set the configuration information Cargo needs to compile your program, these lines (name, version, edition) tell Rust what to use
			* Note that the 'edition' is a key that will be meintioned in Appendix E
	- The last line
