# <center> RISC-V Arch Test </center>

## *<center> Implementation of Task 4 </center>*

#### Question Statement:

###### *Write an assembly test to check mstatus.FS and mstatus.SD behavior*

1. Assembly test:
	- Write a test to check the mstatus.FS filed (OFF, CLEAN and DIRTY) (How can you check mstatus.SD field using mstatus.FS? Figure out yourself).
	- The test should be self checking.

#### Build & Run:

###### *Compile Assembly File to Elf:*

```shell
riscv64-unknown-elf-gcc -march=rv32g -mabi=ilp32 -nostdlib -T link.ld task4.S -o test.elf
```
###### *Create a Disassembly:*

```shell
riscv64-unknown-elf-objdump -D test.elf > test.disass
```

###### *Simulate on Spike & Generate Logfile:*

```shell
spike --isa=rv32gc -l --log-commits test.elf 1> spike.out 2> spike.log
```

###### *Simulate on Sail & Generate Logfile:*

```shell
riscv_sim_RV32 test.elf --trace=step 2> sail.out 1> sail.log
```

#### Documentation:

###### *Source Code Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/task4.S
	</span>

###### *Log Files Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/spike.log
	</span>
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Code/sail.log
	</span>

###### *Report Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Report/RISC-V_Arch_Test_Task_4_Report.docx
	</span>

###### *Output Screenshots Available at:*
-	<span style = 
			"color: rgb(255, 64, 92);
			background: rgb(228, 228, 228);
			padding: 4px 12px;
			border-radius: 10px"
		> /Screenshots
	</span>