# Data-aware extension of bpmn.io

[![CI](https://github.com/bpmn-io/bpmn-js-token-simulation/workflows/CI/badge.svg)](https://github.com/bpmn-io/bpmn-js-token-simulation/actions?query=workflow%3ACI)

A tool for modelling data-aware BPMN with simulation capablities, inspired by delta-BPMN and built as a [bpmn-js](https://github.com/bpmn-io/bpmn-js) extension.

[![Screencast](docs/screenshot.png)](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1)

Try it on the [classic booking example](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1&diagram=https%3A%2F%2Fraw.githubusercontent.com%2Fbpmn-io%2Fbpmn-js-token-simulation%2Fmaster%2Ftest%2Fspec%2Fbooking.bpmn) or checkout the [full capability demo](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1&diagram=https%3A%2F%2Fraw.githubusercontent.com%2Fbpmn-io%2Fbpmn-js-token-simulation%2Fmaster%2Fexample%2Fresources%2Fall.bpmn).



## Overview

Upon startup all the standard bpmn.io functions are avaliable and layout is the same as the standard bpmn.io, except these new buttons. 

![Alt text](images/overview.PNG)
The top button toggles between the modeler mode and the simulation mode. The bottom 3 button are for defining process variables, initiate the database and download the diagram. The download button downloads a BPMN file, this can then be dragged and drop into any modeler with this extension. The process variables button opens a text field where the user can define process variables of the format ‘#[variable name] : [value]’, the variable names must be unique, and the value can be a number or a string, no quotes necessary. All variables must be separated with semicolon. 

![some text](images/processVar.PNG) 

The database button, shows a simple textfield with a simple JSON-database file, this file can be altered to what ever is needed, this will later be where the user give the details for their actual database for initiation. If the JSON format is followed, then the database will be initated.  Modelling can now take place.

![somex](images/database.PNG)

## Turtorial
1. Use the small blue button in the bottom of the element menu to create a data task or open the element pallet by clicking on an element.

![](images/newTask.PNG)
2.	Click the dropdown menu button, in the bottom of the data task. This reveals the precondition and effect fields. Before writing make sure that the database if initiated, if not the parser will alert the user.

3.	Now begin writing either the preconditions or the effects, if no precondition is defined, then the effects will immediately take hold when the task is executed. If the you want to access any of the attributes in any table, write select and press TAB, this will show every table, then write ‘.’ And press TAB again to see every attribute in the table. If you already know the attributes needed and their table write a normal SQL query, but it needs to be of the form SELECT A1,…,AN FROM R1,…,RN WHERE condition. If ambious statements are wirtten the parser will catch that not show the green outline, ambigoutiy is solved by using the format Table.Attribute.
![](images/fullTask.PNG)

## Clone, Build and Run

Start by cloning this project, then prepare the project by installing all dependencies using npm:

```sh
npm install
```

Then, depending on your use-case you may run any of the following commands:

```sh
# build the library and run all tests
npm run all

# run the full development setup
npm run dev

# spin up the example with server
npm run start:example2
```


## Additional Resources

* [delta-BPMN](https://link.springer.com/chapter/10.1007/978-3-030-85469-0_13) - The framework used as the foundation for this extension.
* [Token simulation](https://github.com/bpmn-io/bpmn-js-token-simulation) - More info about the simulator and its internals



## Licence

MIT
