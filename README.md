# StudyCode

## c++代码

```c
#include <iostream>
#include <windows.h>
//#include <conio.h>

using namespace std;

/*
    int key;
    key = getch();
    cout<<key<<endl;
    获取键位键值
*/
int main(){
    int val[] = {'C',107,107,160,'Z','H','E','N','H','A','O','W','A','N',32};
    SetCursorPos(100,330);
    for(int i=0;i<2;i++){
        mouse_event(MOUSEEVENTF_LEFTDOWN|MOUSEEVENTF_LEFTUP,0,0,0,0);
    }
    Sleep(1000);
    for(int i=0;i<15;i++){
        keybd_event(val[i],0,0,0);
        keybd_event(val[i],0,KEYEVENTF_KEYUP,0);
        Sleep(30);
    }
    
    return 0;
}
```

*** 
