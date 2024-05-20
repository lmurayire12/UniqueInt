This program reads integers from a text file, filters out any invalid integers, and writes the unique integers to a new text file. It also calculates and prints the runtime and memory usage of the program.

Requirements
Python 3.x
psutil library (install using pip install psutil)

Usage
Place the input text files in the sample_inputs directory.
Run the program.
The program will create a new text file with the same name as the input file in the sample_results directory.

Code Overview
The UniqueIntProcessor class contains the following methods:
__init__: Initializes the unique_integers attribute as a set.
is_valid_integer: Checks if a string is a valid integer within the range of -1023 to 1023.
process_file: Reads integers from an input file, filters out invalid integers, and writes the unique integers to an output file. It also calculates and prints the runtime and memory usage of the program.
custom_sort: A simple bubble sort implementation for demonstration purposes.
The if __name__ == "__main__": block sets up the input and output directories and processes all the input files in the sample_inputs directory.
