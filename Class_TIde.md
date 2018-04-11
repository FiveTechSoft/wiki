| Datas  | Description |
| ------------- | ------------- |
| oWndMain | The main window of the IDE |
| oFolder | The main folder of the IDE |
| aEditors | An array with all the editors in use from the IDE |
| oEditor | The current selected editor |
| lPhoneMode | A logical value, true or false, if the IDE is in phone mode |
| oFuncList | A listbox with the names of all the functions in the edited source code |
| lScintilla | A logical value, true or false, if the IDE uses Scintilla editors |

| Methods  | Description |
| ------------- | ------------- |
| New() | Constructor |
| PhoneMode() | Organizes the IDE in phone mode |
| OpenFile() | Opens a file |
| SaveFile() | Saves the shown source code to a file |
| SelFile() | Lets the user selects a file from disk |
| Setup() | Shows the settings dialogs of the IDE |
| SetupEditor() | Configures a just created editor |
| CloseFile() | Closes the current edited source code |
| FillFuncList() | Refresh the functions list in the edited source code |