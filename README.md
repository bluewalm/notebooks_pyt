


# Notebooks

This repository demonstrates the usage of the `pytorch_embeddings` module. 
Please follow the below steps to run these notebooks. 

1. Clone this repository.
```
git clone https://github.com/bluewalm/notebooks_pyt.git
cd notebooks_pyt
```

2. Download the `pytorch_embeddings` wheel. 

You can download the `pytorch_embeddings` wheel for the `nvcr.io/nvidia/pytorch:23.10-py3` docker container from our website at: https://bluewalm.com/
When you have successfully downloaded it, unpack the wheel for the appropriate GPU architecture and place it in the same folder this README.md file can be found at. 

| Maxwell | Pascal | Volta | Turing | Ampere
|---------|--------|-------|--------|-------
| sm50 | sm60 | sm70 | sm75 | sm80

The wheels are backward-compatible. Thus, you may use the sm50 wheel on Ampere cards. This will affect performance though. 

3. Build the notebook_pyt Docker container. 
```bash
docker build -t notebook_pyt .
```

3. Start an interactive session in the notebook_pyt container. 
```bash
docker run --gpus=all -it --rm --ipc=host -p 8888:8888 -v ${PWD}:/workspace notebook_pyt:latest
```

4. Start jupyter lab from inside the container. 

```bash
jupyter lab --port=8888 --no-browser --notebook-dir=/workspace/
```
Use a browser to open the appropriate link it gives. Make sure to replace `hostname` with `127.0.0.1` in the link. 

5. Open `basic_notebook.ipynb` or `advanced_notebook.ipynb` and run it step-by-step. 



