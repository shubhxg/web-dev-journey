## Useful built-in modules to work with system and files

you will need to require these modules into your code first: `require(’module’)`

### child processes

used to create sub processes inside your code. for example starting browser etc.

`cp.execSync('windows cmd command')`

`cp.execSync('start firefox https://google.com;');`

### os

used to get information about your system.

`os.arch()` → system arch such as 32 or 64

`os.platform()` → platform such as windows etc

`os.networkInterface()` → returns network details

`os.cpus()` → cpu related

`os.totalmem()` → RAM

`os.freemem()` → free RAM

### path

used to get information about path of files, etc.

`path.extname(filePath)` → extension of the file.

`path.basename()` → actual name of the file

`__dirname` → current directory in which this code is being run

### fs

used to read, write, manipulate files in node

`fs.readFile(fileName, 'utf-8', (err, data) => {})` → read file async

`fs.readFileSync('fileName', 'utf-8')` → read file sync

`fs.writeFileSync(’fileName’, data)` → write file sync

`fs.appendFileSync(’fileName’, data)` → append data into the file

`fs.unlinkSync(fileName)` → delete the file

`fs.mkdirSync(’dirname’)` → make directory

`fs.readdirSync('folderPath')` → returns an array of content of the directory

`fs.existsSync('directory Name')` → returns true/false if directory exists

`fs.rmdirSync('directory name')` → deletes an empty directory