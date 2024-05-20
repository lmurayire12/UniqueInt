# UniqueInt 
This program reads integers from a text file, filters out any invalid integers, and writes the unique integers to a new text file. It also calculates and prints the runtime and memory usage of the program.
## Requirements
- Python 3.x
- psutil library (install using pip install psutil)

## Usage
1. Place the input text files in the sample_inputs directory.
2. Run the program.
3. The program will create a new text file with the same name as the input file in the sample_results directory.

## Code Overview
The `UniqueIntProcessor` class contains the following methods:

- __init__: Initializes the unique_integers attribute as a set.
- is_valid_integer: Checks if a string is a valid integer within the range of -1023 to 1023.
- `process_file`: Reads integers from an input file, filters out invalid integers, and writes the unique integers to an output file. It also calculates and prints the 
   runtime and memory usage of the program.
- `custom_sort`: A simple bubble sort implementation for demonstration purposes.

  The if __name__ == "__main__": block sets up the input and output directories and processes all the input files in the sample_inputs directory.




## Example
Suppose the sample_inputs directory contains the following file:
`input.txt`
```
1
2
3
-1
-1024
hello
1024
1 2
2 3

```
After running the program, the sample_results directory will contain the following file:
`input_results.txt`

```
-1
1
2
3
1024
```
And the program will print the following output:

```
1. Memory Usage: 57344 bytes
2. Runtime: 0.0009999275207519531 seconds
```

## Author
- Lievin MURAYIRE
- GitHub: [lmurayire12](https://github.com/lmurayire12)
