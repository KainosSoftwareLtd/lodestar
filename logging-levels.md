# Logging Levels

Log level output should be controlled by a standard configuration variable, and should usually be set more conservatively in downstream environments to help maintain a good signal:noise ratio and avoid wasting disk space.

#### Trace

Lowest level of output logging, typically used when trying to identify flow through a single function. Method in, method out, etc.

#### Debug

Information that would be diagnostically useful to people other than developers (e.g. ops, admin, support, security) when identifying issues.

Typically, log levels of debug and trace would not be expected to be merged to master/develop unless a deployment was specifically being made to debug or profile some issue. Application code developed and verified as correct by tests should not otherwise have this level of logging left internally when submitted for a merge request.

#### Info

Generally useful information about the behaviour of a function or operation of a service (e.g. user authenticated, service startup/shutdown, scheduled task triggered, config values loaded). It can be useful to keep this level of logging as the default on a development environment.

#### Warn

Any edge case behaviours that result from catching expected exceptions, handling issues in data (e.g. database returning multiple items in a list expected to contain a single element). Any behaviour that can automatically be recovered and worked around but which may be indicative of an underlying issue (e.g. retrying request after timeout, switching from primary to backup nodes).

#### Error

Any error which is fatal to the operation but not the service or application as a whole (e.g. can't read a certain file, missing data in request, serialisation errors etc). Log output of this level may force user intervention (admin alerted or end user retrying). This should be reserved for severe isues - as a developer, expect to get an email about something logged at this level.

#### Fatal

Any error forcing the shutdown of a service or complete inability of an application to fulfil its contract, or an action taken to prevent/halt data loss. This is a critical incident and should be reserved for data corruption or total failure of a major component - as a developer, expect to get a phone call about something logged at this level.