# Stored Procedure To Jupyter Notebook Conversion

This project is about being able to tag your comments and create code blocks within your sql scripts or stored procedures, and convert it with this program into a jupyter notebook (which can be used with .NET Interactive's SQL cells, or Azure Data Studio's Notebook functionality - as it is tested so far.)

* this project is an experiment in a unique way of documenting SQL code
* the following notations are part of this experimental project: 
  * a block comment (start a line with -- BlocCom), which is a comment that is also part of the code,but it is converted to a Markdown cell in the .ipynb file
  * CodeBlocBegin_{number} comments start a code cell in the notebook
  * CodeBlocEnd_{number} comments end a code cell in the notebook- you can use nested code blocks as well
  * BlockToComment_{number} will be commented in the same code cell block as  referred in the CodeBlocBegin_{number} comment
  * BlockToUnCommen_{number} will be uncommented in the same code cell block as  referred in the CodeBlocBegin_{number} comment
  * RemoveDemoWhere: comments will be removed from the code, where the comment is placed- this can help to add specific filters for demonstration purposes
  * RemoveLine_Block_{number} lines will be removed from the code, where the comment is placed- this can help to ensure right syntax in a code cell.

You may change these notations and the regex patterns right in the Program.cs file.

The project has a TestSp2.sql, and a TestSp2.ipynb file, the latter has been created from the former.


