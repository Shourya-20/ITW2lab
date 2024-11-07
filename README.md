# ITW2lab
#!/bin/bash

# Greet the user
echo "Hello, welcome to the Linux demo script!"

# Ask for the filename
echo "Please enter a filename:"
read filename

# Check if the file exists
if [ -e "$filename" ]; then
    echo "The file '$filename' already exists."
else
    echo "The file '$filename' does not exist. Creating it now..."
    # Create the file and write some text into it
    echo "This is a demo file created by the Linux script." > "$filename"
    echo "File '$filename' has been created!"
fi

# Display the contents of the file
echo "Here are the contents of '$filename':"
cat "$filename"

# End the script
echo "Thank you for using the demo script!"
