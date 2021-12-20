# How to test classifier?
---
## [1st step] Prepare data
### If your data looks like this:

| password  | strength |
| ------------- | ------------- |
| qwerty123  | 1  |
| 1qaz!QAZ  | 2  |
| ...  | ...  |
| nikita  | 0  |

### Goto [PrepareYourData.ipynb](PrepareYourData.ipynb)
- write path to your file
- run all cells
#### If you do everything right you should have *DataForTest.csv* file.
### DataForTest.csv:
| password	| len_of_pswd	| is_digit	| is_char	| is_upper	| is_special_characters	| strength | 
| -----------	| ------	| ------	| -------	| ------	| -----	| ----- | 
| kzde5577	| 8	| 1	| 1	| 0	| 0	| 1 | 
| nikita	| 6	| 0	| 1	| 0	| 0	| 0 | 
| 1qaz!QAZ	| 8	| 1	| 1	| 1	| 1	| 2 | 
| ...	| ...	| ...	| ...	| ...	| ...	| ... | 

## [2st step] Test classifier
---
### Goto [BuildingClassifier.ipynb](BuildingClassifier.ipynb)
- run cells one by one
- write path to *DataForTest.csv*
- see the results
- don't run the last cell(its too long)
---
# About files
---
## data.csv 
- Contains raw data.

## Preprocessing and Data Analysis.ipynb
- Contains preprocessing and small data analysis

## Prepared Data
- Data with more columns A.K.A. features:
  - password 
  - len_of_pswd (number of symbols)
  - is_digit (if there is a number)
  - is_char (if there is a character)
  - is_upper (if there is a character in uppercase)
  - is_special_characters (if there is a special character (!@#$%))
  - strength

## BuildingClassifier.ipynb
- Building Suport Vector Machine based on sklearn
