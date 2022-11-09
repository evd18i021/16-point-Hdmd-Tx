# 16-point-Hdmd-Tx
Hadamard transform is non-sinusoidal, orthogonal transformation techniques. A signal is composed of basic functions like harmonics in Fourier Transform.This signal can be divided using these fast transforms. In contrast to the Fourier transform, which uses Nlog2N multiplication and addition and is faster, Hadamard Transform uses Nlog2N addition or subtraction.

The advantage of the discrete Hadamard transform is that it only requires 1 & -1 during
the transformation procedure. This results in an increase in performance but also avoids
multiplication, which significantly lowers the hardware requirement.

Design has been carried out using Skywater 130nm PDK using openLANE and caravel open source silico development tools,
![openlane flow](https://user-images.githubusercontent.com/106398260/200923562-10258199-deb3-4f2c-9889-5fffb18edf0b.jpg)


A 2-point Hadamard matrix is represented as,

![image](https://user-images.githubusercontent.com/106398260/200916745-71ffaf15-d4e9-40d0-8fa0-6eded2f11194.png)

Recursive property of Hadamard matrix allows us to easily generate its M order matrices

![image](https://user-images.githubusercontent.com/106398260/200917431-a13524f4-af09-47cd-a95f-fff0f045cb7a.png)

4-point DHT (Discrete Hadamard Transform) can be instantiated using 2-point DHT and stages can be divided,

![ex2](https://user-images.githubusercontent.com/106398260/200920895-18d07759-c20d-4b66-8080-383a4cef58e2.png)


Similarly 16-point DHT,

![butterfly 16 point Hdmd Tx](https://user-images.githubusercontent.com/106398260/200912744-7210721f-9a68-4bdb-93bc-4dfb3b3bcfa9.png)

Circuit is developed in Verilog HDL using instantiation of 2,4,8 point DHTs which in turn uses adder/subtractor
![image](https://user-images.githubusercontent.com/106398260/200922435-9a479b2f-748f-42b0-9478-5169eeeafcb6.png)

Verilog HDL RTL simulation Waveforms
![combined 6](https://user-images.githubusercontent.com/106398260/200920074-1722c314-1fa6-46ec-a4ef-a6d89479d32e.png)

OpenLANE Flow,

![combined 2](https://user-images.githubusercontent.com/106398260/200921075-787d82c2-355f-4c4f-9a3c-17ec11989529.png)

Caravel and OpenLANE reports for manufacturability,

![combined 5](https://user-images.githubusercontent.com/106398260/200922855-9b7f4ee9-ad3e-4d90-af81-3f6901bb1980.png)

Reports, 

Synthesis Report -
![syn rpt](https://user-images.githubusercontent.com/106398260/200923842-4dde56d9-3eed-429c-997d-70986c9dec91.png)

Power Report -
![power rpt](https://user-images.githubusercontent.com/106398260/200923932-fef7b6c7-7fd3-40da-8c33-72353d239319.png)

Congestion report - 
![cong rpt](https://user-images.githubusercontent.com/106398260/200924171-cf73b80b-f087-4f61-8078-bd7ffb73d837.png)

