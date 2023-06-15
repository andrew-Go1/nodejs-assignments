# Assignment: Node.js basics

## Description

Your task is to complete several simple tasks to learn Node.js basics

Fork [this repository](https://github.com/AlreadyBored/node-nodejs-basics)

Assignment contains several nested folders inside `src`. Your task is to implement necessary functionality inside them

## Technical requirements

- Any external tools and libraries are prohibited
- Use 18 LTS version of Node.js
- Don't change signature of pre-written functions (e.g. don't rename them, don't make them synchronous, etc.)
- Prefer asynchronous API whenever possible

## Subtasks


### :heavy_check_mark: File system (src/fs)


You should implement several functions in dedicated files
- `create.js` - implement function that creates new file `fresh.txt` with content `I am fresh and young` inside of the `files` folder (if file already exists `Error` with message `FS operation failed` must be thrown)

Expand All
	@@ -27,41 +27,41 @@ You should implement several functions in dedicated files
- `list.js` - implement function that prints all array of filenames from `files` folder into console (if `files` folder doesn't exists `Error` with message `FS operation failed` must be thrown)
- `read.js` - implement function that prints content of the `fileToRead.txt` into console (if there's no file `fileToRead.txt` `Error` with message `FS operation failed` must be thrown)


### :heavy_check_mark: Command line interface(src/cli)


You should implement several functions in dedicated files


- `env.js` - implement function that parses environment variables with prefix `RSS_` and prints them to the console in the format `RSS_name1=value1; RSS_name2=value2`
- `args.js` - implement function that parses command line arguments (given in format `--propName value --prop2Name value2`, you don't need to validate it) and prints them to the console in the format `propName is value, prop2Name is value2`


### :x: Modules(src/modules)


You should refactor file (you can add additional imports if needed)


- `cjsToEsm.cjs` - rewrite it to it's equivalent in ECMAScript notation (and rename it to `esm.mjs`)


### :heavy_check_mark: Hash (src/hash)


You should implement several functions in dedicated files


- `calcHash.js` - implement function that calculates SHA256 hash for file `fileToCalculateHashFor.txt` and logs it into console as `hex`


### :heavy_check_mark: Streams (src/streams)


You should implement several functions in dedicated files


- `read.js` - implement function that reads file `fileToRead.txt` content using Readable Stream and prints it's content into `process.stdout`
- `write.js` - implement function that writes `process.stdin` data into file `fileToWrite.txt` content using Writable Stream
- `transform.js` - implement function that reads data from `process.stdin`, reverses text using Transform Stream and then writes it into `process.stdout`


###  :white_check_mark: Zlib (src/zip)


You should implement several functions in dedicated files


- `compress.js` - implement function that compresses file `fileToCompress.txt` to `archive.gz` using `zlib` and Streams API
- `decompress.js` - implement function that decompresses `archive.gz` back to the `fileToCompress.txt` with same content as before compression using `zlib` and Streams API


###  :white_check_mark: Worker Threads (src/wt)


You should implement several functions in dedicated files



Expand All
	@@ -72,10 +72,10 @@ You should implement several functions in dedicated files


The results in the array must be in the same order that the workers were created


###  :white_check_mark: Child Processes (src/cp)


You should implement several functions in dedicated files


- `cp.js` - implement function `spawnChildProcess` that receives array of arguments `args` and creates child process from file `script.js`, passing these `args` to it. This function should create IPC-channel between `stdin` and `stdout` of master process and child process:
    - child process `stdin` should receive input from master process `stdin`
    - child process `stdout` should send data to master process `stdout`

The results in the array must be in the same order that the workers were created

### Child Processes (src/cp)

You should implement several functions in dedicated files

- `cp.js` - implement function `spawnChildProcess` that receives array of arguments `args` and creates child process from file `script.js`, passing these `args` to it. This function should create IPC-channel between `stdin` and `stdout` of master process and child process:
    - child process `stdin` should receive input from master process `stdin`
    - child process `stdout` should send data to master process `stdout`
