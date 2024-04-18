# Variables, Constants and Arguments in Studio

# Variable
Variables in Studio are configured through four main properties. They are as follows:
1.  Name
- attribute that is used to identify a variable
-  a **mandatory** field
-  if you don't add a name to a variable, one is automatically generated
-  the names of the variables must be meaningful and as descriptive as possible
- using the **PascalCase** naming convention

2. Variable Type
- defines the kind of data stored in a variable
- this is a **mandatory** field
- Some of the common data types include
	- Boolean
	- Int32
	- String
	- Object
	- System.Data.DataTable 
	- Array of [T]
- UiPath also supports data types from imported dependencies as well

3. Scope
- defines the context in which a variable can be used in the project
- is a **mandatory** field
- the scope of variables can be set to the current workflow file or any of the container activity within the workflow file
- the scope of variables can also be set to global

4. Default Value
- it is the default value of the variable
- this is an **optional** field
- if a variable is declared with this field empty, then a default value corresponding to the variable's data type is assigned to it

## **Best practices when working with variables**
- Assign meaningful names
- Follow a naming convention
- Keep variables in the innermost scope

## Exploring data types
- data types describe the kind of data a variable can hold
- variables and arguments in Studio need to have a specific data type defined
- data types ensure that the right data format is applied at each stage of an automated process
### Data types
1. String
- store texts - System.String

2. Numeric
- store numbers
- Int32 - System.Int32
- Long - System.Int64
- Double - System.Double

3. Boolean
- store one of two value: True or False

4. Collection
- Array - ArrayOf<T> or System.DataType[]
	- stores multiple values of the same data type
	- the size (number of objects) is defined at creation
- List - System.Collections.Generic.List<T>
	- stores multiple values of the same data type, just like Arrays 
	- the size is dynamic.
- Dictionary - System.Collections.Generic.Dictionary<TKey, TValue>
	- stores objects in the form of (key, value) pairs
	- each of the two can be a separate data type

5. Data Table
- represents variables that can store big pieces of information and act as a database or a simple spreadsheet with rows and columns

6. Date and Time (Category)
- DateTime - System.DateTime
	- stores specific time coordinates (mm/dd/yyyy hh:mm:ss)
	- this kind of variable provides a series of specific processing methods like subtracting days, calculating time remaining vs. today, and so on.
- TimeSpan - Syastem.TimeSpan
	- tores information about a duration (dd:hh:mm:ss)
	- use it to measure the duration between two variables of the type DateTime

### Conversion methods of Data Types
There will be scenarios where we'll need to change the data type of a variable to another form

|Method|Description|Example|
|---|---|---|
|`Convert.ToString`|Converts a value to a string.|`StrVar = Convert.ToString(IntVar)`|
|`Convert.ToInt32`|Converts a string to a 32-bit integer.|`IntVar = Convert.ToInt32(StrVar)`|
|`Double.ToString`|Converts a double value to a string.|`StrVar = DblVar.ToString`|
|`Double.Parse`|Converts a string to a double value.|`DblVar = Double.Parse(StrVar)`|
|`Boolean.ToString`|Converts a Boolean value to a string ("True" or "False").|`StrVar = BooleanVar.ToString()`|
|`Convert.ToBoolean`|Converts a value to Boolean.|`BooleanVar = Convert.ToBoolean(IntVar)`|
|`DateTime.Now`|Gets the current date and time on the computer.|`DateTimeVar = DateTime.Now`|
|`ToString(DateTime)`|Converts a DateTime value to a string.|`StrVar = DateTimeVar.ToString("dd-MM-yyyy")`|
