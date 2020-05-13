Further explanation of the data can be read in the README in the zipped data, "Human Activity Recognition Using Smartphones Dataset - Version 1.0"

The data was transformed in the following ways:

If the required data is not present, the data is pulled from source and unzipped with no modifications.

The following tables are read via "read.table"

activity_labels.txt
features.txt
X_train.txt
y_train.txt
subject_train.txt
X_test.txt
y_test.txt
subject_test.txt
The data frame created from features is used as the variable names in the X-test and training data frames. "Index" is used as the col.name for the Y-test and training data to tie that back to the data frame created from the activity_labels.txt.

The Training and Test rows is combined, then the X- and Y- sets columns are combined with the Subject columns.

The columns are then reduced to those related to the Mean and Standard Deviation, reducing the variable count from 563 to 88.

For each row, the Activity Index Number is changed to the actual name of the Activity, and index is changed to Activity. The Activity names are referenced from activity_labels.txt

The variable names are changed to make them more understandable, these changes are tabulated at the end of the document. Most of the changes revolve around unifying to the greatest extent possible the format, capitals with no spaces, and expanding abbreviations like "acc" to "Accelometer"

A final tidy data table called "data_final" is created grouping the data on Subject and Activity and summarizing the mean of all the grouped variables.
