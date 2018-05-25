# check-gpu

A simple tool for enriching the output of `nvidia-smi`. 

Specifically, `nvidia-smi` shows only PIDs. This simple script also shows usernames of each PID as well

## Usage (if you want to use this at any directory, please add its path to ~/.bashrc

    check_gpu

## Example output
      
    Fri May 25 22:32:56 2018       
    +-----------------------------------------------------------------------------+
    | NVIDIA-SMI 384.111                Driver Version: 384.111                   |
    |-------------------------------+----------------------+----------------------+
    | GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
    | Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
    |===============================+======================+======================|
    |   0  GeForce GTX 108...  Off  | 00000000:0A:00.0 Off |                  N/A |
    | 59%   75C    P5    30W / 250W |    177MiB / 11172MiB |      8%      Default |
    +-------------------------------+----------------------+----------------------+

    +-----------------------------------------------------------------------------+
    | Processes:                                                       GPU Memory |
    |  GPU       PID   Type   Process name                             Usage      |
    |=============================================================================|
    |    0     43749      C   .../build/tools/extract_image_features.bin   167MiB |
    +-----------------------------------------------------------------------------+
    USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
    dangman+ 43749  230  1.5 14535940 258984 pts/11 Rl+ 22:32   0:02 /home/dangmanht
