# **Assignment5**

A program that searches for a specific gene for a specific animal within a data set.

## Description

get_gene_level_information.py is a program that will take two command line arguments (the first being the scientific or common name of an animal and the second being a gene name) and search within a data set what tissues (if any) express that specific gene in the animal. The program will return an alphabetical list of tissues. Several functions are used to execute this program.
def get_dictionary_for_unigene creates a file path to the correct animal, the correct gene, and the correct file name extension (in this case ".unigene"). This programs another module name config.py that adds in this process.
def update_host_name takes the list of available animal names that can be called within the command (this dictionary is created in config.py as well) and correlates the animal name to its scientific name in which the file in the data set if named (ie. the entry of "human" becomes "Homo_sapiens"). 
def _print_dictionaries_for_hosts is a helper function that ensures that the host name leads to a valid data set. If the host name is not valid, the program will output a list of animal names that can be read correctly by the program. The program will then exit.
def get_data_for_gene_file looks within the file that was accessed using the get_dictionary_for_unigene above, and it creates an alphabetical list of tissues that express that gene.
def print_host_to_gene_name_output takes the host name, gene, and list of tissues and outputs them to the terminal for the user to see.
def is_gene_file_valid makes sure that the file path is able to run properly and that the gene being looked at exists. If the file is valid, the program will continue through the rest of the functions. If the file is invalid, the program will print that that gene does not exist for that animal, and it will exit the program.

## Getting Started

### Dependencies
Python verison 3.6 or later is needed to run this code.

The data set that is being evaluated must be able to be called within the terminal when calling any of the above programs. The modules io_utils.py and config.py must also be available for the program to reach.

### Installing
The file named assignment.zip is used to run code described above. It contains get_gene_level_information, config.py, and io_utils.py

### Executing Program
When executing get_gene_level_information.py, use the following format to call the program: python3 get_gene_level_information.py --host1 (insert animal name here) --gene (insert gene name here)

Example: python3 get_gene_level_information.py --host horse --gene API5

The program will execut and produce an output like the following: 

Found Gene API5 for horse
In Equus_caballus, There are 3 tissues that API5 is expressed in:

	  1. Adult
	  2. Blood
	  3. Cartilage


## Authors
Hannah Vaden
Vaden.h@northeastern.edu

## Version History
v.01 Initial Release

## Acknowledgments
* I received assistance with writing the function update_host_name() to assign the correct scientific name the the animal that was enter at the beginning, as well as for additional functions in a test_confic.py test suite that ensures the config.py module need for the program to run was in order. This assitance came from ChatGPT, an AI language model developed by OpenAI.
