JSON JMESPath Query Generator is a Python tool designed to automatically generate JMESPath queries for exploring and extracting data from JSON files. This tool reads a JSON file, recursively traverses its structure, and generates JMESPath queries along with the corresponding results for each path. It helps in understanding the structure of complex JSON data and finding specific information within it.

Features
Recursive Traversal: The tool can handle deeply nested JSON structures by recursively traversing through dictionaries and lists.
Query Generation: Automatically generates JMESPath queries for each data point in the JSON structure.
Result Output: Outputs each JMESPath query along with the result of evaluating that query against the JSON data.
Error Handling: Provides clear error messages if there are issues parsing the JSON file.
How It Works
Read JSON Data: The tool reads JSON data from a specified file.
Generate Queries: It recursively generates JMESPath queries for each piece of data in the JSON structure.
Display Results: Outputs each query and its result, showing how to access various parts of the JSON data.
Code Overview
generate_jmespath_queries
This function recursively traverses the JSON data:

For Dictionaries: Iterates through key-value pairs and constructs JMESPath queries for each value.
For Lists: Iterates through list items and constructs JMESPath queries for each item.
Base Case: Handles primitive data types (strings, numbers, booleans, etc.) by generating queries for their paths.
process_json
This function manages the overall process:

Reads and parses JSON data from a file.
Calls generate_jmespath_queries to generate the queries and results.
Prints the generated queries and their corresponding results.
Handles JSON format errors and provides informative messages.
Usage
To use the tool, specify the path to the JSON file and run the script. The generated JMESPath queries along with their results will be printed to the console.

python
Copy code
input_file = 'json_data_input.json'
process_json(input_file)
Requirements
Python 3.x: The script is written in Python 3 and requires Python 3.x to run.
JSON File: The input JSON file should be properly formatted.
License
This project is licensed under the MIT License - see the LICENSE file for details.
