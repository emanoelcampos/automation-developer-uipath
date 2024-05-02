# String methods  

Below are some of the most common string manipulation methods which are borrowed from VB.NET.

#### String.Concat
- Concatenates one or more instances of string or string representation of objects.  
- Expression: **String.Concat (VarName1, VarName2)**
- Output datatype: **String**
#### Contains
- Checks whether a specified substring occurs within a string and returns either true or false.  
- Expression: **VarName.Contains (“text”)**
- Output datatype: **Boolean**
#### String.Format
- Converts the value of objects to strings and inserts them into another string.   
- Expression: **String.Format(“{0} is {1}”, VarName1, VarName2)**
- Output datatype: **String**
#### IndexOf
- Returns the index position of the first occurrence of a specified character or a substring. 
- Expression: VarName1.IndexOf(“a”)
- Output datatype: Int32
#### LastIndexOf
- Returns the index position of the last occurrence of a specified character or a substring.
- Expression: **VarName1.LastIndexOf("author")**
- Output datatype: **Int32**
#### String.Join
- Concatenates the elements in a collection using the specified separator and displays them as a String.  
- Expression: **String.Join(“|”, CollVarName1)**
- Output datatype: **String**
#### Replace
- Replaces all the occurrences of a substring in a string.  
- Expression: **VarName.Replace (“original”, “replaced”)**
- Output datatype: **String**
#### Split
- Splits a string into substrings using the specified separator.  
- Expression: **VarName.Split(“|“c)(index)**
- Output datatype: **Array of String**
#### Substring
- Extracts a substring from a string using the starting index and the length.  
- Expression: **VarName1.Substring(startIndex, length)**
- Output datatype: **String**
