# AuxilliaryProject


 ### Task 1: Write a shell script to ask users for their name, age and output a message with their name and year they were born?

 #!/bin/bash

echo "What is your name?"
read name

echo "What is your age?"
read age

current_year=$(date +%Y)
birth_year=$((current_year - age))

echo "Hello $name, you were born in $birth_year."

==========================================================

 ### Task 2: write a shell script to create a new directory with a name provided by the user, and navigate into it?

 #!/bin/bash

echo "Enter the name of the new directory:"
read directory_name

mkdir "$directory_name"
cd "$directory_name"

echo "New directory created: $directory_name"

========================================================

### Task 3: write a shell script to List all files in the current directory, sorted by file size?

#!/bin/bash

ls -Slh

=========================================================

### Task 4: write a shell script to count the number of files in the current directory and output the result.