  
# Working with dictionaries

- Dictionary variables (**Dictionary<TKey, TValue>**) are collection type of variables of (key, value) pairs, in which the keys are unique.
- The data types for both keys and values have to be chosen when the variable is declared.
- The operations that are most often associated with dictionaries are:
	- Adding and deleting (key, value) pairs.
	- Retrieving the value associated with a key.
	- Re-assigning new values to existing keys.

## Methods for working with dictionary variables:

### Initialization
- As in the case of list variables, dictionary variables need to be initialized as well. For example, if we want to initialize a dictionary of **String type of key** and **String type of value**, we can add **new Dictionary(Of String, String)** inside the **Default** value field in the **Variables** panel or **Data Manager** panel for the respective variable, or use an **Assign** activity to assign the value to the variable within the workflow.
### Adding Key-Value Pairs
- **VarName.Add(Key, Value)** adds an item to an existing dictionary variable. Because **Add** doesn't return a value, we use the **Invoke Method** or **Assign** activity.
### Removing Keys
- **VarName.Remove(Key)** removes an item from the dictionary variable. It can be used in an **Invoke Method** activity. 
### Retrieving
- **VarName.Item(Key)** returns the Dictionary item by its key.
- **VarName.Count** returns an Int32 value of the number of Dictionary items.
- **VarName.ContainsKey(Key)** checks if the item with the given key exists in the dictionary variable and returns a **Boolean** result.
