# **Project1-sequence-analysis**
## Title & Purpose
Program analyses next-generation sequencing (NGS) reads comparing each read against a reference sequence to identify mutations. Aiming to investigate whether mutation patterns differ in treatment and control samples. 

## How to Run the Program
Open C7147_Project_1_assessment.ipynb in Google colab and run all notebook cells in order. First the setup code to load reference sequence and read dataset. Then the analysis using necessary functions.

## Inputs and Outputs
The program expects a reference DNA sequence and reads dataset, stored as dictionaries containing read identifier, sample names, group names and nucleotide sequences. The output includes validation results, identified, mutation, mismatch summaries, substitution counts, position counts and comparison between statistics of control and treatment group. Results displayed as table and summary statistics.

## Code design
The later functions required a good understanding of how the data was structured, so I kept examples of the data output next to the functions while developing the code. This made it easier to understand the nested dictionaries being created and helped with debugging when values were being stored incorrectly.

When calculating substitution counts and position counts, I simplified the code by analysing both within the same mutation loop rather than creating separate loops, which reduced code repetition and improved readability while producing the same output.

I also used helper functions like find_top_positions() in Step 4 which reduced repetition in the Step 5. Additional functions were used in creating summary tables making output easier and debugging errors faster.

## Testing 
I tested the program using normal, edge-case and invalid inputs. First, tested valid reads with a matching reference sequences to confirm mutations were detected properly. Then tested invalid reads containing either a wrong length or wrong nucleotide character. I also tested edge-case such as empty inputs with mutation to ensure functions are working well and return expected results.
