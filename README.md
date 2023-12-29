# Real-time video enhancement on FPGA
Real-time video upsampling by four times using bicubic interpolation on FPGA, which minimizes the usage of resources (DSP48 blocks) and memory. (MIT 6.111 Project) ([Report](report.pdf), [Slides](https://github.com/sjb565/Fpgesture-controlled-video-enhancement/blob/main/Project%20Presentation.pdf), [Video](https://www.youtube.com/watch?v=FiGxE-KXj5g))  

![Sample Results from the Hardware Implementation on FPGA](<sample_result.png>)

## Software Verification Codes
The codes for software verification of our design is located in [software testbench](<software testbench>).
* [gerenate_filter_coefficient.nb](https://github.com/sjb565/fpga-video-enhancement/blob/main/software%20testbench/generate_filter_coefficient.nb): generate upsampling filter coefficients on wolfram notebook
* [bicubic.py](https://github.com/sjb565/fpga-video-enhancement/blob/main/software%20testbench/bicubic.py): compares hardcoded bicubic interpolation coefficients vs. OpenCV upsampling methods
* [kernel_tb.ipynb](https://github.com/sjb565/fpga-video-enhancement/blob/main/software%20testbench/kernel_tb.ipynb): auto-generates random image patches and appropriate testbenches for each upsampling kernel type
* [filter_types.txt](https://github.com/sjb565/fpga-video-enhancement/blob/main/software%20testbench/filter_types.txt): definition of each upsampling filter used in systemverilog files
