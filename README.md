# Task-14-Pandas-Series-Basics.
Objective
Understand and practice the Pandas Series, a one-dimensional data structure in Python. This task covers creating Series, custom indexes, indexing, filtering, arithmetic operations, and basic statistical analysis.
Tools Required
Python
Pandas
Jupyter Notebook (or Google Colab)
1. Install and import Pandas
If Pandas is not installed, run:
!pip install pandas
Import the library:
import pandas as pd
2. Create a Pandas Series
A Series stores a sequence of values with labels (called an index).
import pandas as pd

marks = pd.Series([85, 90, 78, 92, 88])
print(marks)
The default index is 0, 1, 2, ....
3. Create a Series with a custom index
marks = pd.Series(
    [85, 90, 78, 92],
    index=["Anu", "Balu", "Charan", "Divya"]
)
print(marks)
Here, student names are the index labels.
4. Access Series elements (indexing)
print(marks["Anu"])       # Access using a label
print(marks.iloc[1])      # Access using a position
.loc[] accesses values by index label.
.iloc[] accesses values by integer position.
5. Filter Series values
print(marks[marks >= 85])
This displays only the marks that are 85 or above.
6. Perform arithmetic operations
print(marks + 5)   # Add 5 to every value
print(marks * 2)   # Multiply every value by 2
Pandas performs these operations on each element.
7. Basic statistical operations
print("Sum:", marks.sum())
print("Mean:", marks.mean())
print("Maximum:", marks.max())
print("Minimum:", marks.min())
print("Count:", marks.count())
print("Summary:")
print(marks.describe())
describe() gives a quick statistical summary, including count, mean, standard deviation, minimum, quartiles, and maximum.
8. Complete practice program
import pandas as pd

marks = pd.Series(
    [85, 90, 78, 92, 88],
    index=["Anu", "Balu", "Charan", "Divya", "Esha"]
)

print("Student Marks:")
print(marks)

print("\\nMark of Balu:")
print(marks["Balu"])

print("\\nStudents scoring 85 or above:")
print(marks[marks >= 85])

print("\\nAdding 5 grace marks:")
print(marks + 5)

print("\\nStatistical Summary:")
print(marks.describe())
Expected Learning Outcomes
After completing this task, you should be able to: 1. Create a Pandas Series using pd.Series(). 2. Create and use custom indexes. 3. Access values using labels and positions. 4. Filter values based on conditions. 5. Perform arithmetic operations on Series. 6. Calculate basic statistics and use describe().
Conclusion
A Pandas Series is a useful one-dimensional data structure for storing and analyzing labeled data. This task demonstrates its basic creation, indexing, filtering, arithmetic, and statistical features.
