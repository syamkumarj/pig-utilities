A pig script can't be run multiple times successfully without changing its output directories or removing the directories. It becomes a repeated task when the pig scripts are to be run multiple times for various validations. When the number of output directories are more in number, the manual effort increases. For improving the time taken, this solution is used

how to run -

1. Save the sh file in hadoop (let us say it is saved as test.sh)
2. Execute the command chmod a+x test.sh
3. Create a file which contains the list of pig script names of which the output is to be cleansed. (referred here after file name as input)
4. Run the script as ./test.sh input
5. The output directories will be cleansed only if the current user has permissions, otherwise the script will end gracefully.