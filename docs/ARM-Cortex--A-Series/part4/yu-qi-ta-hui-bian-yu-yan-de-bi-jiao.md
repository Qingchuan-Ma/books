## 与其他汇编语言的比较

ARM 处理器是一种简化指令集计算机\(Reduced Instruction Set Computer——RISC\)处理器。复杂指令集计算机\(Complex  
 Instruction Set Computer ——CISC\)处理器，如x86，有一个丰富的指令集，能够用一条指令做复杂的事情。这种处理器通常具有大量的内部逻辑，可以将机器指令解码为内部操作序列\(微代码\)。与此相反，RISC 体系结构有更少的通用指令，可以使用更少的晶体管来执行，使得硅更便宜，更节能。和其他 RISC 体系结构一样，ARM 内核有大量的通用寄存器和许多在单循环中执行的指令。它有简单的寻址模式，所有的加载/存储地址都可以从寄存器内容和指令字段中确定。

ARMv7 架构具有基本的数据处理指令，允许内核执行算术操作（如 `ADD`）和逻辑位操作（如`AND`）。它们还将程序执行从程序的一个部分转移到另一个部分，以支持循环和条件语句。该体系结构还具有读写外部内存的指令。

ARM 指令集通常被认为是简单、逻辑和高效的。它具有某些处理器所不具备的特性，同时却也缺乏其他处理器所具备的操作。例如，它不能直接在内存上执行数据处理操作。要在内存位置中增加一个值，必须将该值加载到 ARM 寄存器中，寄存器更新，并且需要第三条指令将更新后的值写入到内存中。指令集体系结构\(Instruction Set Architecture——ISA\)包括

1. 结合了算数或逻辑操作的移位指令
2. 为最优化程序循环而存在的自增加和自减少寻址模式
3. 以支持高效的堆栈和堆操作的加载和存储多指令
4. 块复制功能和条件执行几乎所有指令

与 x86 \(但与 68K 不同\)一样，ARM 指令通常有两到三个操作数格式，第一个操作数在大多数情况下指定结果的目的地。加载多个和存储指令是这个规则的例外。而 68K 则将目的地作为最后一个操作数。对于 ARM 指令，对于哪些寄存器可以用作操作数通常没有限制。Example 4-1 和 Example 4-2 给出了不同汇编语言之间的差异。![](../assets/example4-1.png)![](../assets/example4-2.png)



