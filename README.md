# Online Judge Assistant

![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)

Today, I want to contribute to Codeforces community, because I received much benefit and fun 
from Codeforces and I appreciate for them. 

Online Judge Assistant is designed for Codeforces and the other online judge system. It can create files quickly for the Codeforces contests.The files can create from custom template locally.

## Feature
- Auto create source code files(.cpp;.java) from contest or single problem.
- Custom source code(.cpp;.java) template.

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

## How to custom source C++ code template
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

## How to custom source java code template
- Create file template.java in installed directory.
- You can edit your template.java  like this:
```java
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

import java.io.*;
import java.util.*;

public class {fileNameNoExtension}
{
    public static void main(String[] args) throws IOException
    {
        boolean isLocal= System.getProperty("ONLINE_JUDGE") == null;
        long startTime = 0;
        if (isLocal)
        {
            startTime = System.currentTimeMillis();
            //redirect stdin/stdout to local file
            System.setIn(new FileInputStream(new File("{fileNameNoExtension}.in")));
            System.setOut(new PrintStream(new File("{fileNameNoExtension}.out")));
        }

        FastReader in = new FastReader(System.in);
        PrintStream out = System.out;

        new Solution(in, out).Solve();

        out.close();
        
        if (isLocal)
        {
            System.err.println("program exited after: " + (System.currentTimeMillis() - startTime) + "ms");
        }        
    }

    private static class FastReader
    {
        private BufferedReader reader;
        private StringTokenizer tokenizer;
    
        public FastReader(InputStream input)
        {
            reader = new BufferedReader(new InputStreamReader(input));
            tokenizer = new StringTokenizer("");
        }
    
        public String next()
        {
            while (!tokenizer.hasMoreTokens())
            {
                // TODO add check for eof if necessary
                try
                {
                    tokenizer = new StringTokenizer(reader.readLine());
                } catch (IOException e)
                {
                    e.printStackTrace();
                }
                
            }
            return tokenizer.nextToken();
        }
    
        public int nextInt()
        {
            return Integer.parseInt(next());
        }

        public long nextLong()
        {
            return Long.parseLong(next());
        }
    
        public double nextDouble()
        {
            return Double.parseDouble(next());
        }

        String nextLine()
        { 
            String str = ""; 
            try
            { 
                str = reader.readLine(); 
            } 
            catch (IOException e) 
            { 
                e.printStackTrace(); 
            } 
            return str; 
        }         
    }    

    private static class Solution
    {
        private FastReader In;
        private PrintStream Out;

        public Solution(FastReader in, PrintStream out)
        {
            this.In = in;
            this.Out = out;
        }

        public void Solve()
        {
            Out.println("OK");
        }
    }
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


## How to use Online Judge Assistant in IntelliJ IDEA
todo

## Demonstration
![](OJAssistantUI.gif)
