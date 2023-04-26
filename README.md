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

#!/bin/bash

file_count=$(ls -1 | wc -l)

echo "The number of files in the current directory is: $file_count"

=========================================================

### Task 5: write a shell script to make a list of numbers as input from the user and output the sum of those numbers.

#!/bin/bash

echo "Enter a list of numbers separated by spaces:"
read number_list

sum=0
for num in $number_list
do
    sum=$((sum + num))
done

echo "The sum of the numbers is: $sum"

========================================================

### Task 6: write a shell script to output a random number between 1 and 100

#!/bin/bash

echo $((1 + RANDOM % 100))

========================================================

### Task 7: write a shell script to create a backup of a specified file by copying it to a backup directory with a timestamp in the filename

#!/bin/bash

backup_dir="/path/to/backup/directory"

echo "Enter the filename to backup:"
read filename

if [ -f "$filename" ]
then
    backup_filename="$backup_dir/$(date +%Y-%m-%d_%H-%M-%S)_$filename"
    cp "$filename" "$backup_filename"
    echo "Backup created: $backup_filename"
else
    echo "File not found: $filename"
fi

======================================================

### Task 8: write a shell script to check if a website is online and output a message indicating whether it is up or down

#!/bin/bash

echo "Enter the website URL to check:"
read url

if curl --output /dev/null --silent --head --fail "$url"
then
    echo "$url is up"
else
    echo "$url is down"
fi

==================================================

### Task 9: write a shell script to convert a temperature in Celsius to Fahrenheit, using input from the user

#!/bin/bash

echo "Enter a temperature in Celsius:"
read celsius

fahrenheit=$(echo "scale=2; ($celsius * 1.8) + 32" | bc)

echo "$celsius degrees Celsius is $fahrenheit degrees Fahrenheit."

=====================================================

### Task 10: write a shell script to Ask the user for a sentence, then output the sentence in reverse order

#!/bin/bash

echo "Enter a sentence:"
read sentence

reversed=$(echo $sentence | rev)

echo "Reversed sentence: $reversed"

=======================================================



