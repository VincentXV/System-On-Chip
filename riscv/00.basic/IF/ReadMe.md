# Compile Command
## Test Source
* 需要在`2025_SoC_code/riscv/00.basic/IF/testSource`底下執行
* 指令：
    ```bash=
    $ make
    $ make hex
    ```
* Makefile還要再細讀，仍有些東西不懂
## Test Bench
* 需要在`2025_SoC_code/riscv/00.basic/IF`底下執行
* 指令：
    ```bash=
    $ verilator -Wall --cc --exe --build testbench.cpp sim_mem.cpp inst_fetch.v --trace
    $ make -C obj_dir -f Vinst_fetch.mk
    $ ./obj_dir/Vinst_fetch
    $ gtkwave wave.vcd
    ```