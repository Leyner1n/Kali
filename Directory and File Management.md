
## ==*Files Management*==

### Represent (Предоставление)
	ls - shows files in directory

	KEYS:
		-l -> detailed info
		-a -> all files + hidden(.cfg, .git)

### Permission (Разрешения)
	chmod [options] [file or folder]

### Create
	touch (date yyyy/mm/dd/hh/mm) [new_file]
	
	echo -> using to show text in terminal or add txt to file 
		echo [text] > [file]
			- "\n" - new line
			- "\t" - tabulation 

### Delete 
	rm -> deleting option
		rm [option] file

	Tags:
		"-r" -> delete info inside a folder (recursively)
		"-i" -> ask before delete
		"-f" -> delete without questions
		"-r *" -> delete all files in directory

		(You cat folding this commands)

### Copying/Removing/Renaming

	cp -> coping info
		cp [option] [where to copy]
		cp [file] [file whith another name]

	mv -> moving info
		mw [option] [where to move]]

### Search

	locate -> fast search

	which -> where are been command

	find -> powerfull search (reliable(надежный))

		Tags:
			"." -> currrent folder 
			"-iname" -> case-insensitive (без учета регистра)


## ==*Compress*==
**(.tar, .gz, .bz2, .zip)**
### tar
**tar (Archive)** - tape archive (Linux standard) 

	Archiving

	tar [oprions] [archive_name].tar [file0 [file1]]
		Options:
			"-c" -> create (creating archive)
			"-v" -> verbose (show the process)
			"-f" -> file (archive name)
					(also keeps folding)

	UnArchiving

	tar [options] [archive_name]
		Options:
			"-x" -> extract
			"-v" -> verbose
			"-f" -> archived file
					(also keeps folding)

	Archive + Compression Keys:
		"-z" -> .tar.gz/.tgz
		"-j" -> .tar.bz2/.tbz2
		"-J" -> .tar.xz/.txz

### gz
**.gz (Compression)** - archive type, created for compression information, it curried out using (осуществляется за счет) ==gzip==  
**gzip** - utility for (de)compression files 


==! .gz = 1 file it can't keep more !== .gz can compress folder but it not combine to 1 file

	Packing:
		gzip [file]

	UnPacking: 
		gunzip [file] or gzip -d [file]

	Options: 
		"-d" -> Decompressing
		"-k" -> Con't kill original file
		"-c" -> Return result in the terminal (stdout (standart out))
		"-r" -> Compressing all files in folder
		"-v" -> Compression ratio + capacity - before/after
		"-(1-9)" -> Compression levl
		"-t" -> checking file integrity(целостность)
		"-l" -> inforation list 

![[File Formats Difrences.canvas]]
### bz 
**.bz2  (Compression)**- Compression utility (stronger than .gz) (b -> burrows (норы), 2 -> format version)

	bzip2 [file] -> create [file.txt.bzip2] and kill [file.txt]

	Suporting Options:
		"-d" - decompress
		"-k" - keep
		"-t" - test
		"-v" - verbose (подробный)


### xz
**.xz (Compression)** - modern compression format

	xz [file] 
	tar -cJf [file](.tar.xz)
	
### zip
**.zip (Compression + Archive)** - utility for create ZIP-archive 
(zip universal Archive type in OS's)

	zip [archive_name] [file] ([other_files])

	Options:
		"-r" 
		"-j" -> saved files whithout fileStructure (all in Archive root)
		"q" -> quite mode (less info in the terminal)
		"-u" -> adds only new files

## ==*Directory Management*==

### Display 
	ls - shows files in directory

	KEYS:
		-l -> detailed info
		-a -> all files + hidden(.cfg, .git)

**Change the current one**
	`cd [directory_path]`

 **Print the current now**
	`pwd(Print Working Directory)`

	Options:
		"-L" -> Logical Path (/home/user/Documents)(symilink)
		"-P" -> Physical (/mnt/storage/Docs)
### Create

	mkdir [dirrctory_name]

	Options:
		"-p" -> create nested(вложенные) directories
		"-v" -> creating message
		
		"-m MODE" -> setting access rights
			Example:
				"mkdir -m 755 myfolder"
### Delete
	rm [file]

	Options:
		"-f" -> force
		"-i" -> ask before running the command
		"-r(R)" - recursive (all directory)
		"-v" - verbose (what was deleted)

### Copy/Remove/Rename
	cp -> coping info
		cp [option] [where to copy]
		cp [file] [file whith another name]

	mv -> moving info
		mw [option] [where to move]]

### Mounting
	mount [dir0] [dir1 to dir0]
	Options:
		"-t" -> select the file system type
		"-o" ->  mounting options (ro, rw, rx...)
			Syntax:
				"mount -o ro [[dir0] [dir1 to dir0]]"
		"--bind" -> create mirror directory
				Options:
					"-o"
			Syntax:
				mount --bind dir0] [dir1 to dir0]
				mount --bind -o ro dir0] [dir1 to dir0]

	umount [dir] === umount [dir_path]
	Options:
		"-a" -> umount all file system
		"-l" -> lazy umount (umount FS when it is free)
		"-v" -> verbose

## ==*Text Files*==
### Display
	cat - command for create/viewing/combine(объеденять) files
		cat [file] - show
		cat > [file] - create (Ctrl+D = Save)
		cat >> [file] - add text
			Options: 
				"-n" -> numver each line
				"-b" -> number not-empty lines
				"-s" -> kill empty lines

	head/tail [file] - show the beginning/ending of the file 
		Options:
			"-n [num]" -> how many lines you want to see
			"-c [num]" -> how many bytes of infomation you want to see

### Fast Paste
	echo - print/write text 
	Usage Option:
		1. echo [word] -> print [word] in terminal
		2. echo [word] > [file] -> overwtite file
		3. echo [word] >> [file] -> add [word] to the end of file
		4. echo [variable] -> print variable 
	Options:
		"-n" -> whithout lines breaks
		"-e" -> switch off special symbol
			Sample:
				"-n", "-t" 
				
### Editors
	vim - strong graphic editor 
		it can create/eddit files
		Usage Variables:
			1. vim [non-existent_file] -> create file
			2. vim [existen_file] -> edid mode
###### **How To Use ?... [[Vim]]** 

	nano - simply than Vim (better for beginners)
	Usage Variables:
		1. nano [non-existent_file] -> create file
		2. nano [existen_file] -> edid mode
###### **How To Use ?... [[Nano]]** 

### Sort
	sort [option] [file]
	Example:
		sort [file] -> sort by alphabet
		sort -t ":" -k 2 -n -u [file]
	Options:
		"-r" -> reverse
		"-n" -> sort by number
		"-k" -> sort by column
		"-t" -> sort by [char]
		"-u" -> sort by uniqueness
		"-f" -> ignore the word case(регистр)
		"-" -> ignore the extra spaces

	uniq [option] [file] - rather useful tool for "sort", it using to sort by uniqueness but more options then "sort -u [file]"
	Example:
		sort [file] | uniq [option]
	Options: 
		"-c" -> repeat counter
		"-d" -> show only repeating lines
		"-u" -> show only uniqueness lines
### Search

**grep** - is a strong command to search or print according to a certain(по определенному) pattern 

Decoding -> g/re/p - Global/Regular Expression/Pattern

	grep [word] [file.txt] - Simply Variable
	Options: 
		"-i" -> ignore the word case
		"-v" -> print NUMBERS of LINES whitout template ("-v" [template])
		"-n" -> show line numbers
		"-c" -> line counter
		"-L" - print FILES whitout template ("-L" [template]) -> [files]
		"-l" - print FILES WITH template -> [files]
		"-r" - recursive search in directory -> [files]
		"-w" -> print lines with [word]
		"-o" -> print only [word]
		"--color" -> highlight template

###### Grep Supports [[MetaCharacters]]

	awk - text edit bu columns (search/edit) 
	Syntax: awk '{print}' file.txt (will print like "cat")

	Variables:
		"$(number)" -> (number) column
		"$0" -> all string 
		"NF" -> column count

... i''ll write about [[awk]] later, this topic very extensive

	cut [option] [file]
	Options: 
		-c [num-to-num]" -> cut by char range 
		
		"-d" - spliter
		"-d" - the numbering 
	
		"cut -d [char] -f [num] [file/path]"
	
test 