# What is involved in an automation implementation process

1. Capturing the 'as-is' and 'to-be' process steps
- the business analyst is the one who captures all the *'as-is'* and *'to-be'* process step.
2. Documenting the process steps
- the process steps are thoroughly documented within the Process Definition Document (PDD) and validated with the Solution Architect.
3. Signing-off the PDD
- it is the **Project Manager**'s responsibility to **obtain sign-off on the documented PDD** from the business team.
4. Designing the solution
- the Solution Design stage of the implementation process begins. 
- the Solution Architect designs a future state flow and maps out the various modules to be developed to complete the automation.
5. Developing the solution
- the **Automation Developers** create the modules outlined in the design whiteboard using the PDD and Solution Design Document (SDD) as references.  
- Deciding between attended or unattended automation is the first important decision that impacts how we build the code.  
    Making a change to the robot type later in the phase may prove to be quite complicated.
    
- Choosing the correct type of layout for the project in Studio is also essential. We can choose from sequences, flowcharts, and state machines.
    
- We must also ensure that we have installed the required dependencies to use the activities needed for the automation.
    
- When developing workflows, we should also consider automation best practices, such as using a centralized knowledge repository, source control, Workflow Analyzer, etc.