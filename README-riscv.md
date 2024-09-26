# Use riscv-gnu-toolchain to run llama.c

主要的想法是用riscv的工具链将llama.c编译成riscv指令的可执行文件，然后再通过
使用qemu运行大模型。

编译指令：

```
make run CC=riscv64-linux-gnu-gcc
```

运行qemu指令：

```
qemu-riscv64 ./run stories15M.bin -i  "I have a story about little prince"
```
