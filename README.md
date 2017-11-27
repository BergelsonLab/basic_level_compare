# basic_level_compare

basic_level_compare.py takes 3 arguments, big, small, and two_or_three

big is the path of the basic_level file that has a greater number of rows
small is the path of the basic_level file that has a smaller number of rows
two_or_three is either 2 or 3, which determines whether to match against two criteria (word and ordinal/tier) or 3 criteria (word, ordinal/tier, and onset) when determining whether the files have common rows with values changed

basic_level_compare looks at the big and small basic_level files to compare them and outputs two csv files: 

one with all of the rows common to both files but had some value changed, data_common_to_but_different_in_[bigger file name]_and_[smaller file name].csv
one with the rows that exist in the first but not the file, data_only_in_[bigger file name]_and_not_[smaller file name].csv


compare_basic_level reads in the files as pandas Dataframes and uses the .merge method to compare them on the appropriate values.




