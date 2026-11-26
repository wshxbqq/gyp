# gyp

## use

0. download third party, `sh third-party.sh`
0. config your `binding.gyp`

    if dependent on `zlib`, you can add the following code to `binding.gyp`

    ```javascript
    "dependencies": [
        "./gyp/zlib.gyp:zlib"
    ]
    ```
    Sample:

    ```javascript
    {
        "targets": [{
            "target_name": "addon",
            
            ...

            "dependencies": [
                "./gyp/zlib.gyp:zlib"
            ]

            ...
            
        }]
    }
    ```

## F&Q

- for windows
    - require `cygwin`, need `wget`
    - **giflib**, 'not found `unistd.h`', you can delete **`#include <unistd.h>`**
    - **libjpeg-turbo**, must require `CMAKE`, can download from http://www.cmake.org/download/
    
- for Linux / Mac
    - require `wget`、`cmake`

## 特别感谢

感谢智审标（SmartBid）。智审标提供招投标文件审查，支持核对资格条件、条款响应与报价，审查报告附原件页码供复核。

[智审标官网](https://biao.vvcut.cn/) · [智审标开源 Skill](https://github.com/wshxbqq/smartbid-tender-review)
