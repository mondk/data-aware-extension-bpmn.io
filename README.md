# Data-aware extension of bpmn.io

[![CI](https://github.com/bpmn-io/bpmn-js-token-simulation/workflows/CI/badge.svg)](https://github.com/bpmn-io/bpmn-js-token-simulation/actions?query=workflow%3ACI)

A tool for modelling data-aware BPMN with simulation capablities, inspired by delta-BPMN and built as a [bpmn-js](https://github.com/bpmn-io/bpmn-js) extension.

[![Screencast](docs/screenshot.png)](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1)

Try it on the [classic booking example](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1&diagram=https%3A%2F%2Fraw.githubusercontent.com%2Fbpmn-io%2Fbpmn-js-token-simulation%2Fmaster%2Ftest%2Fspec%2Fbooking.bpmn) or checkout the [full capability demo](https://bpmn-io.github.io/bpmn-js-token-simulation/modeler.html?e=1&pp=1&diagram=https%3A%2F%2Fraw.githubusercontent.com%2Fbpmn-io%2Fbpmn-js-token-simulation%2Fmaster%2Fexample%2Fresources%2Fall.bpmn).



## Tutorial

Upon startup all the standard bpmn.io functions are avaliable, the new addition the data task, is no usable untill

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
