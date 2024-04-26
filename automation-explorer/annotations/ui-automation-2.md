# Introduction to Activities, Activity Properties, and Input Methods

## UI automation activities

UI automation activities enable developers to create instructions that instruct the robot to interact with various applications' interfaces.

1. Containers
- These activities identify the browsers or applications that the process needs to interact with.
- The Container will execute all activities within it on the same application. 
- These activities include Open Browser, Attach Browser, Open Application, and Use Application/Browser. 

2. Activities for Synchronization
- These activities enable the Robot to perform specific actions when specific events on the machine occur based on the UI behavior.

3. Input Activities
- These activities are used to input data into user interface elements. 
- Other examples would be clicking, checking, typing into, or sending hotkeys. 

4. Output Activities
- These activities are used retrieve information from GUI Elements. 
- They can instruct the Robot to get text by using various methods, get structured data, or retrieve UI Elements containing images.

## Activity properties

UI Automation activities have different sets of properties depending on the type of activity. Below is an illustration of the types of properties used in UI Automation activities.

| **Property**                   | **What it does**                                                                    |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| **DelayAfter**/**DelayBefore** | How many milliseconds the robot waits before or after executing the activity.       |
| **ContinueOnError**            | Specifies if the automation should continue even when the activity throws an error. |
| **Target**                     | Provides several properties related to identifying the target UI Element.           |
| **Timeout (seconds)**          | How many milliseconds will the Robot try to perform an action on a UI element.      |
| **Input Mode**                 | What input method do we use for input activities.                                   |
| **Output**                     | It Stores the output of the activity in the form of variables.                      |
## Input methods

Whenever we insert data into an application or send a command to a system to produce a change or continue, we perform an input action.


1. Hardware Events
- Hardware events are essentially the actions we perform using our keyboard or mouse, such as clicking or typing. 
- One important thing to note is that hardware events are compatible with all applications but do not work in the background. This means that the attended user cannot touch the mouse or keyboard during the automation.

2. SendWindowMessages
- It simulate user interactions with an application. 
- When you use this input method, UiPath sends the same messages to an application that the application would receive if a user were to interact with it using a keyboard or mouse. 
- The benefit of using Send Window Messages is that it allows the automation to work in the background without interfering with the user's ability to use their computer.

3. Simulate
- Simulate input method designed to mimic our actions in a way that's similar to how we would interact with the application. This means that instead of relying on low-level hardware events or window messages, Simulate can interact with UI elements directly.
- By doing this, the robot can perform actions such as clicking a button or typing in a text box more accurately and consistently.
- Additionally, using Simulate is often faster than using hardware events or window messages, and allows the robot to interact with an application in the background while we perform other tasks.

4. ChromiumAPI
- ChromiumAPI is an input method used for browser automation, and it's based on the Devtools protocol. It's compatible with all Chromium-based browsers, such as Chrome or Edge.
- ChromiumAPI supports several activities including Use Application/Browser, Click, Type Into, Hover, and Keyboard Shortcuts.
- It uses direct communication with the browser, which means there are fewer communication channels and increased automation reliability.
- One of the advantages of using ChromiumAPI is that it works in the background, allowing users to work on other activities while the automation is executing.

Here are the differences between each input method.

| Input Method       | Compatibility                                | Background Execution | Speed | Hotkey Support | Auto Empty Field |
| ------------------ | -------------------------------------------- | -------------------- | ----- | -------------- | ---------------- |
| Hardware Events    | 100%  - all types of applications.           | No                   | 50%   | Yes            | No               |
| SendWindowMessages | 80%                                          | Yes                  | 50%   | Yes            | No               |
| Simulate           | 99% - web apps  <br>  <br>60% - desktop apps | Yes                  | 100%  | No             | Yes              |
| ChromiumAPI        | 100% - Chrome and  Edge browsers             | Yes                  | 50%   | Yes            | Yes              |
## 'Use Application/Browser' Activity Properties

- The "Use Application/Browser" activity opens either a web browser page or desktop application for use in UI automation.
- Using a project-relative path is possible by copying the application folder to the project folder.
- "Input" settings configure the target application.
- "Arguments" pass parameters at startup, like opening a specific file.
- "File path" specifies the executable file to open, clearing the URL.
- "Open" chooses when to open the app: Never, IfNotOpen (default), or Always.
- "Resize window" resizes the app at initialization: None, Maximize, Restore to current size, or Minimize.
- "Window attach mode" chooses where inner activities search for their target elements: Application instance or Single window. 
- "Close" chooses when to close the app: Never, IfOpenedByAppBrowser (default), or Always.