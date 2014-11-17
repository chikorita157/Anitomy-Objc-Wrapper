# What is this
This is a wrapper for Anitomy, which parses anime video filenames. This wrapper makes it possible to use this C++ library with Cocoa/Objective C.

#Demo
Demo is [here](https://github.com/chikorita157/Anitomy-Objc-Wrapper-demo)

#How to use
Insert this to the Prefix Header File
```h
#ifdef __cplusplus
#include <stdlib.h>
#endif
```

Include anitomy-bridge.h to the class. Here is example code:
```m
    NSDictionary * d = [[anitomy_bridge alloc] tokenize:@"[Chibiki]_THE_iDOLM@STER_-_01_[720p][C83E5732].mkv"];
    NSLog(@"%@",d);
```

Should output the following:
```
{
    episode = 01;
    group = Chibiki;
    releaseversion = "";
    title = "THE iDOLM@STER";
    videosource = "";
    videoterm = "";
    year = "";
}
```

#License
The bridge class is licensed under [GNU General Public License v3](https://www.gnu.org/licenses/gpl-3.0.html).