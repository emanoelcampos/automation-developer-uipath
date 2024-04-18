# Arguments
Arguments are elements that are very similar to variables. They store data dynamically, have the same data types, and support the same methods and properties as variables.

## Workflow
A workflow represents a relatively small piece of an automation project, typically executing a specific part of the process. Once built, it can be reused across different projects.
- workflow is made of Studio activities, interconnected through variables to form a routine
- routine typically has an input and an output
- it defines the flow of automation
- UiPath Studio provides you with predefined workflow layouts
	- Sequences
	- Flowcharts
	- State Machines
- the fastest, most reliable, and useful way of automating a process is to break it down into smaller bits
- this allows for independent testing of components, enables team collaboration, and component reuse

## Argument x Variable
- while variables pass data between activities, arguments pass data between workflows
- an additional property associated with arguments is the direction
- arguments have specific directions: **In**, **Out**, and **In/Out**
- this tells the Robot where the information stored in them is supposed to go.

## Best practices when working with arguments and workflow files
- Assign meaningful names
- Follow a naming convention
- Use prefixes in argument names
	- argument names should have a prefix stating the argument type, such as in_DefaultTimeout, in_FileName, out_TextResult, io_RetryNumber.
- Use action verbs in workflow names
	- except for Main, all workflow names should contain the verb describing what the workflow does, such as GetTransactionData, ProcessTransaction, TakeScreenshot.


|**Variables**|**Arguments**|
|---|---|
|Don't have directions like In, Out, or In/Out.|Do have directions like In, Out, In/Out.|
|To create a variable press: Ctrl + K.|To create an In Argument press: Ctrl +M. To create an Out Argument press: Ctrl+Shift+M.|
|To create variables, there must be at least one activity in the Designer Panel.|Arguments can be created if the Designer panel doesn't contain any activity.|
|Require a defined scope.|Do not require a scope.
