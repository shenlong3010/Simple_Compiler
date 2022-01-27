# Simple_Compiler
Inspired by Brian Robert Callahan in https://briancallahan.net/blog/20210814.html

Note: This is just good enough compiler, not state-of-the-art clang or gcc compiler. This is just for learning purpose.\n

Developed on: tux - Unix server built from Drexel.\n

A language to compile: PL/o (https://en.wikipedia.org/wiki/PL/0)\n
A language to implement PL/o compiler: C\n
Development environment: unix\n
IDE: vim\n

Workflow:\n
+-------+\m
| Start |\m
+-------+\m
    |\m
    +---+\m
        |\m
        V\m
+----------------+    +------------+      -------      +--------+\m
| Read in a line |    | Parse into |     /       \  No | Write  |\m
|                |--->|            |--->| Pass 1? |--->|        |\m
| of assembly    |    | tokens     |     \       /     | binary |\m
+----------------+    +------------+      -------      +--------+\m
        ^                                    |             |\m
        |                                    | Yes         |\m
        |                                    |             |\m
        |                                    V             |\m
        |                               +---------+        |\m
        |                               | Record  |        |\m
        |                               | address |        |\m
        |                               +---------+        |\m
        |                                    |             V\m
        |                                    |       -----------\n
        |                                    |  No  / End of    \\n
        +------------------------------------+-----|             |\n
                                                    \ assembly? /\n
                                                     -----------\n
                                                           |\n
                                                           | Yes\n
                                                           |\n
                                                           V\n
                                                        +-----+\n
                                                        | End |\n
                                                        +-----+\n
