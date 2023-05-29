
# Configure Vscode for using cppcheck with Misra C

To install and configure cppcheck in vscode, you have to follow the following steps:

## Install cppcheck

* sudo apt install cppcheck

## Install cpp flylint extension

* CTRL + P and then paste "ext install jbenden.c-cpp-flylint"

## Configure vscode with cpp flylint

* CTRL + SHIFT + P and then open "Settings"
* Clang: Enable = false
* Cppcheck: Enable = true
* Flawfinder: Enable = false
* Lizard: Enable = false
* In "C-cpp-flynt > Cppcheck: Addons", you should modify the setting.json file adding the following code:

```json
    "c-cpp-flylint.cppcheck.addons": [ 
    "misra"
    ]
```

After restarting vscode, if you have written code which violates the MISRA C standard the problem section will show you errors and the relative suggestions to follow in order to avoid them.
