### Config Recipe ###

Config recipe has been created to easily store a global string or object. That's why the api is separated into two parts, `src/api/object` and `src/api/string`. The api verbs are the same for both part, and they consist of :

* get<Type>Config
* list<Type>Config
* remove<Type>Config
* set<Type>Config

Where <Type> is Object or String, depending on the type you want to manipulate. The config recipe will manipulate a Gda table impersonating a global user, and simplify you the use of a shared storage.
