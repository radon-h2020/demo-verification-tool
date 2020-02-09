# RADON Verification Tool Demo

Welcome to the Demo page for the RADON Verification Tool.

The RADON Constraint Definition Language (CDL) provides a way of
expressing the high level functional and non-functional requirements of
a FaaS architecture. The final version of the associated Verification
Tool (VT) will have three main modes of execution, detailed below.

1. Verification. In this mode, the tool checks whether a given RADON model complies with
the constraints expressed in a given CDL specification.
2. Correction. In this mode, the tool searches for a modification of a (non-compliant)
RADON model, in order to make it comply with the constraints in a given CDL
specification.
3. Learning. In this mode, the tool is given examples of valid and invalid RADON models,
or execution traces, and a partial CDL specification. The tool then searches for an
extension of the CDL specification which rules out all of the invalid examples, which
maintaining consistency with the valid examples.

The current version of the VT supports the first two modes of execution.

To request a license to use the demo, please go to [fill out this
form](https://imperial.eu.qualtrics.com/jfe/form/SV_1HthWM3xILQM6ih).

## Instructions

The demo is a simple web interface, available
[here](http://ec2-18-220-31-32.us-east-2.compute.amazonaws.com/).

To get started, you can select one of the examples in the dropdown. It
is also possible to start from a blank specification and try your own
example. For more information on what it is possible to write in the
CDL, please see [this
document](http://radon-h2020.eu/wp-content/uploads/2020/01/D4.1-Constraint-definition-language-I.pdf).

All examples return results in verification mode. The correction mode
relies on a search space of potential extensions of the RADON model,
which has only been given for the Function Pre/Post Condition
Verification task. For all other tasks, the tool will return
UNSATISFIABLE in this mode (which is the correct answer, as there are no
valid extensions in the empty search space).

## Demo Limitations

To ensure the responsiveness of this site, there is a timeout of 15s on
all computation. This means that some more complex tasks (such as the
race conditions example in [Deliverable
4.1](http://radon-h2020.eu/wp-content/uploads/2020/01/D4.1-Constraint-definition-language-I.pdf)
are not possible.

This simple web interface assumes that the specification is written in a
single file. You can still import files from the CDL standard library
(using #import <...>) and can still import the example RADON model shown
here. It is not currently possible to edit the RADON model through the
web interface (although this is obviously possible when using the full
command line version of the Verification Tool).
