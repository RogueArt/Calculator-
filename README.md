## About

**This is a joke project**. This is an 8 million line hard-coded calculator. This repo does not contain the files directly as they were too large for Git/Github to handle. As such, the .zip file contains a Java program to print 8 million lines of Python code to console. The resulting Python code is a CLI tool that takes two inputs and adds them. 

## Getting Started

If you wish to compile the raw version yourself (not recommended, this can literally take an hour since it prints to stdout), here are the instructions.

### Prerequisites
1. Download Java
```sh
sudo apt-get update
sudo apt-get install adoptopenjdk-11-hotspot
```
For Windows users, you can download it fromm [here](https://adoptopenjdk.net/).

2. Download Python
```
sudo apt-get update
sudo apt-get install python3.6
```
For Windows users, you can download it from [here](https://www.python.org/).

3. Run the Java program to build the Python script using
```
javac calculator++.java
```

4. Save the console output and paste it to a .py file. Then run it using
```
py calculator++.py
```

## Goals

1. Redirect output to a text file rather than to stdout. This prevents slowdown from excessive memory usage.

2. Rewrite as high-performance, multithreaded, cache-optimized Rust code to generate this script.

3. Compile to serializable formats for easy execution by other languages.

4. Write an algorithm to compress the raw data to make this as portable as possible. 

The goal would be to utilize high-performance techniques to generate as many lines in the shortest amount of time as possible.  Given that 1 million bytes of sequential writes in main memory take around 5 microseconds, a naive/non-concurrent Rust version should then take only 2 milliseconds for 4,000,000 lines with 50 bytes of text on them. A multithreaded program will be **much** faster although who needs that much speed?
