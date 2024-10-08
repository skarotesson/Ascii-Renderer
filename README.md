Toy project to render 3D graphics in the terminal.

**Compile and Run:**
```
$ make
$ ./out
```

**Code structure:**
- The main function of interest is the `float fragment(int x, int y);` function. It functions similarly to a fragment shader in OpenGL.
- The character set used to represent brightness is stored in a string in `char brightness_encode(float brightness);`.
- The function, `void render(float output_buffer[WIDTH][HEIGHT]);` calls the fragment function for each cell, passes the resut through brightness_encode to map the brightness to a character, and writes to an output buffer which is displayed after each frame.

Example snapshot from rendering a sphere with a directional light:
```





                                           &&&&&888888%%%%
                                      ##MMMWWWW&&&&&888888%%%%%
                                  khaooo###MMMWWWW&&&&&&88888%%%%%B
                                dbkhhaaooo###MMMMWWWW&&&&&&88888%%%%%
                              mqpdbkkhhaaaoo####MMMMWWWW&&&&&888888%%%%
                            LOmwqpddbkkhhaaaooo###MMMMWWWWW&&&&&88888%%%%
                          uUL0Omwqqpdbbkkhhhaaooo####MMMMWWWWW&&&&&88888%%%
                         jcYJL0OZmwqppdbbkkkhhaaaooo####MMMMWWWW&&&&&88888%%
                        )juzUJLQOZmwwqppddbbkkhhaaaoooo###MMMMMWWWW&&&&&8888%
                       l)txvzYJLQ0OZmwwqppddbbkkhhhaaaooo####MMMMWWWWW&&&&888%
                       i{\fxvzYUCLQ0OZmwwqppddbbkkkhhhaaaooo####MMMMWWWW&&&&88
                       I?)/fxucXUJCLQ0OZmwwqqppddbbkkhhhaaaoooo###MMMMWWWW&&&&8
                       ^~[)/frnvzYUJCLQ0OZmmwqqppddbbbkkhhhaaaoooo###MMMMWWWW&&
                        :~]1\tjxuczYUJCLQ0OZZmwwqqppddbbkkkhhhaaaooo####MMMWWWW
                         :~?{|/frnvcXYUJCLQ0OOZmmwqqppdddbbkkkhhhaaaooo####MMMW
                          ,i-})\*frnvcXYUJCLQ00OZZmwwqqppdddbbkkkhhhaaaooo###MM
                           ^I+]{(\*jrnvczXUJCCLQ0OOZmmwwqqppdddbbkkkhhhaaaooo##
                             :!_]{(\*frnuvzXYUJCLLQ0OOZmmwwqqpppddbbbkkhhhaaaao
                              `;i_[{(\*fjxnvczXYUJCLQQ0OOZZmmwwqqppdddbbkkkhhh
                                ^;i_]{)|/tjrnuvczXYUJCLLQ00OZZmmwwqqqppdddbbbb
                                  ^;!+?}1(\*tjrnuvczXYUJJCLQQ00OZZmmmwwqqqppp
                                     ,l~-]}1(\*tjrxuvczXXYUJCCLLQ00OOOZZmmmZ
                                       ^:!~-]}1(\/tfjxnuvczzXYUUJJCLLLQQQQC
                                          ^:l~_?[{)|\/tfjrxnuvcczXXXYYYYX
                                             `,I!~_?[{1(|\/*tfjrxxxnnxr
                                                 `";li+_?]}{1)((|||(1
                                                       `":;Il!!!l;




Time (s): 5.350015
```







