## 实现用户界面


### 直接加载 ui 文件

```python
import sys
from PyQt5.QtWidgets import *
from PyQt5.QtCore import *
from PyQt5.QtGui import *
from PyQt5.uic import loadUi

class MyDialog(QDialog):
    def __init__(self,parent = None):
        super(MyDialog, self).__init__(parent)
        loadUi("findandreplacedlg.ui",self)

if __name__ is "__main__":
    app = QApplication(sys.argv)
    mywindow = MyDialog()
    mywindow.show()
    sys.exit(app.exec_())
```


### 转换成 py 文件导入


```python
import sys
from PyQt5.QtWidgets import *
from PyQt5.QtCore import *
from PyQt5.QtGui import *
from ui_findandreplacedlg import Ui_FindAndReplaceDlg

class MyDialog(QDialog):
    def __init__(self,parent = None):
        super(MyDialog, self).__init__(parent)
        self.ui = Ui_FindAndReplaceDlg()
        self.ui.setupUi(self)

if __name__ is "__main__":
    app = QApplication(sys.argv)
    mywindow = MyDialog()
    mywindow.show()
    sys.exit(app.exec_())
```
