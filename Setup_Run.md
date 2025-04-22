# Setup
## Python
For this assignment I used python3.9, installed via the following
```bash
add-apt-repository ppa:deadsnakes/ppa
apt update
apt install python3.9 python3.9-distutils
```
## Python Packages
I used the following packages

```bash
python3.9 -m pip install numpy pandas transformers datasets evaluate accelerate jupyterlab
```
For torch I used an installation that matched the cuda version I had installed (I will omit those instructions as they are lengthy and machine dependent). You can follow
the [pytorch install](https://pytorch.org/get-started/locally/) instructions to get a pip command that matches your environment.
```bash
python3.9 -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu126
```

# Running
Once the environment is setup I used Jupyter Lab for running the code. That can be launched via the following command. The extra options can be ommited depending on environment.
For myself I had a docker container running in WSL and these were what I had to use. 
```bash
jupyter lab --allow-root --port=8887 --no-browser --ip=0.0.0.0
```


# Docker Container
In the repository is an exported docker container `ml_docker.tar` file. This can then be imported as a new image with the following command
```bash
docker import ml_docker.tar <new image name>
```
A new docker container will still need to be created with the newly imported image.
