# vLLM Quickstart Notebook
This repository contains a Jupyter notebook that executes the vLLM Quickstart guide.
## Contents
vllm_quickstart.ipynb: A Jupyter notebook replicating the steps in the vLLM Quickstart guide.
## Usage
- I have used `socat` library to do the port forwarding from the server to my localhost, so that I can connect to local runtime from google colab.
- To install on mac, run `brew install socat`. For linux use instructions on `https://www.baeldung.com/linux/socat-command`.
- Install `socat` for your OS and run
`socat tcp-listen:8888,bind=127.0.0.1,fork tcp:<provided-ip-address>:8888`.
- Open google colab and connect to local runtime with address `http://localhost:8888/?token=<provided-token>`
- After connected you can go to `File > Open notebook > Github` and paste `https://github.com/saurabh1043/vllm-notebook/blob/main/vllm_quickstart.ipynb`.
- Now you can start executing the cells in the notebook.
