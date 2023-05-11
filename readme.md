![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Revisiting Machine Learning Case Study

- In this lab, you will use `learningSet.csv` file which we used during the class. 

### Instructions

Complete the following steps on the categorical columns in the dataset:

- Check for null values in all the columns
- Create a new empty list called `drop_list`. We will append to this list a set of columns to be droped later. Add the following columns to this:
    - `OSOURCE` - symbol definitions not provided, too many categories
    - `ZIP` - we are including state already
- Identify columns that over 85% missing values and add them to the previous list.
- Remove the columns included in the `drop_list` from the dataframe
- Now, reduce the number of categories in the column `GENDER`. The column should only have either "M" for males, "F" for females, and "other" for all the rest
    - Note that there are a few null values in the column. We will first replace those null values using the code below:

    ```python
    print(categorical['GENDER'].value_counts())
    categorical['GENDER'] = categorical['GENDER'].fillna('F')
    ```



