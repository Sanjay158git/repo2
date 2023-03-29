	import time 
	import os

These lines import two modules in Python: time, which provides functions for working with time and date, and os, which provides a way to interact with the operating system, such as listing directories and opening files.

	start_time = time.time()

This line sets the start_time variable to the current time using the time.time() function from the time module. This will be used later to calculate how long the script takes to execute.

	directory_path = ''

This line sets the directory_path variable to a string that represents the directory path where the script will search for files.

	keyword = 'sampletest'

This line sets the keyword variable to a string that represents the keyword that the script will search for in each file.

	file_list = os.listdir(directory_path)

This line uses the os.listdir() function to create a list of filenames in the directory_path directory. The filenames will be stored in the file_list variable.

	num_files = 0

This line sets the num_files variable to zero. This variable will be used to count how many files in the directory contain the keyword.

	for file_name in file_list:

This line starts a loop that will iterate over each filename in the file_list variable.

	if file_name.endswith('.txt'):

This line checks whether the current file_name ends with the “.txt” extension, indicating that it is a text file.

	with open(os.path.join(directory_path, file_name), 'r') as f: contents = f.read()

This line uses the open() function to open the current file_name with read-only (‘r’) mode, and reads the contents of the file into the contents variable. The os.path.join() function is used to create a full path to the file by joining the directory_path and file_name strings.

	if keyword in contents: print('Found keyword in file:', file_name) print(contents) num_files += 1

This line checks whether the keyword string is present in the contents variable, and if so, it prints a message indicating that the keyword was found in the file_name file, prints the contents of the file, and increments the num_files variable by 1.

	if num_files == 0: print('Keyword not found in any file')

This line checks whether num_files is still zero, indicating that the keyword was not found in any files. If so, it prints a message indicating that the keyword was not found.

	end_time = time.time()

This line sets the end_time variable to the current time using the time.time() function from the time module.

	print('Number of files searched:', len(file_list)) print('Number of files with keyword:', num_files) print('Execution time:', end_time - start_time)

These lines print out some information about the search, including the number of files searched, the number of files containing the keyword, and the execution time of the script.
