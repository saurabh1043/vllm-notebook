# vLLM Quickstart Notebook
This repository contains a Jupyter notebook that executes the vLLM Quickstart guide.
## Contents
vllm_quickstart.ipynb: A Jupyter notebook replicating the steps in the vLLM Quickstart guide.
## Steps followed
- Created an Azure VM (euivalent to EC2)
- Installed vLLM with CPU support along with jupyter.
- Created an Azure VM Image (euivalent to EC2 AMI)
- Used the image created to spin up a new Azure VM
- Exposed port 8888 for inbound traffic.
- Created the required .ipynb file and put it on a public github repo (this repo).
- Used `socat` library to make the <vm-ip>:8888 available as localhost:8888 for colab to connect.
## Usage
- I have used `socat` library to do the port forwarding from the server to my localhost, so that I can connect to local runtime from google colab.
- To install on mac, run `brew install socat`. For linux use instructions on `https://www.baeldung.com/linux/socat-command`.
- Install `socat` for your OS and run
`socat tcp-listen:8888,bind=127.0.0.1,fork tcp:<provided-ip-address>:8888`.
- Open google colab and connect to local runtime with address `http://localhost:8888/?token=<provided-token>`
- After connected you can go to `File > Open notebook > Github` and paste `https://github.com/saurabh1043/vllm-notebook/blob/main/vllm_quickstart.ipynb`.
- Now you can start executing the cells in the notebook.
