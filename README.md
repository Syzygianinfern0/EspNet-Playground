# EspNet-Playground
💬 Spin Up of an End-to-End Speech Processing Toolkit

The installation notebook can be used for local installation too (it's hard to figure out how to do it from the official docs)


Pre-requisites:
- NVida Drivers
- Cuda
    - Arch Based:
        ```bash
        $ sudo pacman -S cuda
        ```
    - Debain Based:
        ```bash
        # Add NVIDIA package repositories
        $ wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.1.243-1_amd64.deb
        $ sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
        $ sudo dpkg -i cuda-repo-ubuntu1804_10.1.243-1_amd64.deb
        $ sudo apt-get update
        $ wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
        $ sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
        $ sudo apt-get update

        # Install NVIDIA driver (if you dont have it already)
        # Reboot. Check that GPUs are visible using the command: nvidia-smi

        # Install development and runtime libraries (~4GB)
        $ sudo apt-get install --no-install-recommends \
            cuda-10-1 \
            libcudnn7=7.6.4.38-1+cuda10.1  \
            libcudnn7-dev=7.6.4.38-1+cuda10.1
        ```
- Basic Speech Processing Libs
  - Arch Based:
    ```bash
    sudo pacman -S cmake sox libsndfile ffmpeg flac gcc8 bc
    ```
  - Debian Based:
      ```bash
      sudo apt-get install cmake sox libsndfile1-dev ffmpeg flac g++-7 bc
      ```

- GCC version < 8
  - Flag CC and CXX to use them (important) or they wont compile any of the libraries 🤒

Visit EspNet: https://github.com/espnet