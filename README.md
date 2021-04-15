# Online Judge Assistant

![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)

Today, I want to contribute to Codeforces community, because I received much benefit and fun 
from Codeforces and I appreciate for them. 

Online Judge Assistant is designed for Codeforces and the other online judge system. It can create files quickly for the Codeforces contests.The files can create from custom template locally.

## System requirements

- Windows Vista SP2/7 SP1/8.x/10 
- Windows Server 2008 R2 SP1 (64-bit)
- Windows Server 2012 and 2012 R2 (64-bit)
- Windows Server 2016 +
- RAM: 128 MB, Disk space: 10 MB
- Processor: Minimum Pentium 2 266 MHz processor
- Microsoft .NET Framework 4

## How to use
- unpack the release zip file.
- run OJAssistantUI.exe.
- enjoy!

## How to custom source code template
- Create file template.cpp in installed directory.
- You can edit your template.cpp  like this:

```cpp
/*
-------------------------------------------------------------------
* @Name:           {Name}
* @Author:         {Author}
* @Create Time:    {CreateTime}
* @Url:            {Url}
* @Description:    {Description}
-------------------------------------------------------------------
      _
     /(|
    (  :
   __\  \  _____
 (____)  `|
(____)|   |
 (____).__|
  (___)__.|_____

*/

#include <bits/stdc++.h>
using namespace std;

using ll = long long int;

int main()
{

#ifndef ONLINE_JUDGE
    freopen("{fileNameNoExtension}.in", "r", stdin);
    freopen("{fileNameNoExtension}.out", "w", stdout);
#endif

    return 0;
}
```



The program auto fill fields when create file:

| field name              | description                                                              | 
| ---------               | -------------------------------------------------------------- | 
| {Name}                  | the problem name from online judge.                            |       
| {Author}                | coder name.                            |       
| {CreateTime}            | date time when create the file.                            |       
| {Url}                   | the problem url from online judge.                            |       
| {Description}           | the problem Description from online judge.                            |       
| {fileNameNoExtension}   | auto fileName without Extension.                            |       


## Demonstration
![](OJAssistantUI.gif)
