[![Build Status](https://travis-ci.org/MoOmEeN/endo2java.svg?branch=master)](https://travis-ci.org/MoOmEeN/endo2java)

Endomondo
===
In October 2020, Under Armour announced that Endomondo would be shutting down.<br>
Try MapMyRun: https://www.mapmyrun.com/

Endo2Java
=========================

This is a Java implementation of unofficial mobile API of Endomondo.

#### Login ####
```java
EndomondoSession session = new EndomondoSession(userName, password);
try {
	session.login();
} catch (LoginException e) {
	LOG.error("exception while trying to login user: {}", userName, e);
}
```

#### Retrieve data ####
```java
session.getAllWorkouts() // basic data, without gps information
session.getWorkout(id) // single workout, all available data (with gps)
session.getAccountInfo()
```
