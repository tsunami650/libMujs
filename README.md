## Easy-to-use Interface Wrapper for [MuJS](https://github.com/ccxvii/mujs) <sup>1</sup>

First of all, many thanks to the authors of [MuJS](https://github.com/ccxvii/mujs) for providing an excellent embeddable javascript interpreter.  

### libMujs is a simple and easy to use interface to MuJS, and includes these features in addition to the vanilla libmujs:

* Windows-based message queue for thread management and data synchronization between script and process threads.
* ```require``` - function used to load new external javascript modules (file system based).
* ```mujs_bind_c_function``` - With a built-in JS to C++ method routing function, which is forwarded through the bindings.
* ```mujs_evalute_js``` - To execute the js fragment but will push to the bottom of the message queue, and finally execute and then use parameters to determine whether to asynchronous
* ```mujs_call_js_function``` - Used to actively call js function, the parameter is temporarily set to a vector, don't ask me why it doesnt support every data type, the use of mujs is very lightweight.
* ```mujs_show_builtin_function``` -  to see which of the built-in functions are provided by libMujs,
* ```setTimeout, setInterval``` - Important common window object functions missing from the core mujs. ```setTimeout``` execution must run in the original thread context, and until proper marshalling is added, the only supported method for the function execution is through a string to be executed.  This will be improved later to work more like the native ```setTimeout``` and related functions.

Originally built using **VisualStudio 2013** which does not have a complete **C++11** feature set, so this project remains **C++98,03** compatible.

---
<sup>1</sup> Auto-translated (with some editing) from the Chinese [libMujs/README.md](https://github.com/fatezhou/libMujs/blob/master/README.md) to english by [tsunami650](https://github.com/tsunami650/)



