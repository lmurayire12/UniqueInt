# UniqueInt Processor

## Overview
`UniqueInt Processor` is a Python script designed to read integers from text files, filter out duplicates, and write the unique integers into output files. The integers are processed to be within the range of -1023 to 1023, inclusive.

## Features
- Reads integers from input files
- Filters out duplicate integers
- Ensures integers are within the specified range (-1023 to 1023)
- Writes sorted unique integers to output files
- Provides processing time for each file

## Prerequisites
- Python 3.x

## File Structure
- **inputs**: Directory containing the input text files with integers
- **results**: Directory where the output files with unique sorted integers will be saved

## Installation
Clone the repository to your local machine:

```bash
git clone https://github.com/Mkellia/UniqueInt.git
cd UniqueInt
```

## Usage
1. Ensure your input text files are placed in the `inputs` directory.
2. Run the script:

```bash
python3 processor.py
```

The script will read each `.txt` file in the `inputs` directory, process the integers, and save the results in the `results` directory with `_results.txt` appended to the original filename.

## Example
### Input: `/home/kellia/UniqueInt/inputs/numbers.txt`
```
10
20
-15
10
30
-15
20
1024
-1024
```

### Output: `/home/kellia/UniqueInt/results/numbers.txt_results.txt`
```
-15
10
20
30
```

## Code Explanation
### Class `UniqueInt`
- **Attributes**:
  - `seen`: A list of boolean values to track seen integers.
  - `min_int`: Minimum integer value, set to -1023.

- **Methods**:
  - `process_file(input_file_path, output_file_path)`: Resets the seen array and processes the file.
  - `read_unique_integers(input_file_path)`: Reads integers, filters duplicates, and validates the range.
  - `is_valid_integer_line(line)`: Checks if a line is a valid integer.
  - `sort_unique_numbers(numbers)`: Sorts the list of unique integers using bubble sort.
  - `write_unique_integers(unique_numbers, output_file_path)`: Writes the unique integers to the output file.

### Main Execution
- Sets the input and output folder paths.
- Creates an instance of `UniqueInt`.
- Processes each `.txt` file in the input folder and writes the result to the output folder.
- Logs the processing time for each file.

## Notes
- The script uses bubble sort for simplicity, which is not the most efficient sorting algorithm for large datasets. Consider using Python's built-in sorting methods for better performance on larger files.

## Author
- Kellia MUZIRA
- GitHub: [Mkellia](https://github.com/Mkellia)
