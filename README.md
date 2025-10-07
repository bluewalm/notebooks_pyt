
# Notebooks

This repository demonstrates the usage of the bluewalm module. 
Please follow the below steps to run these notebooks. 

1. Obtain the bluewalm pytorch module from us. You can find us at [this place](https://www.bluewalm.com). 
Build the bluewalm Docker container with the Dockerfile obtained from us. 

2. Clone this repository.
```
git clone https://github.com/bluewalm/notebooks_pyt.git
cd notebooks_pyt
```

3. Start an interactive session in the notebook_pyt container. 
```bash
docker run --gpus=all -it --rm --ipc=host -p 8888:8888 -v ${PWD}:/workspace bluewalm_pyt:latest
```

4. Start jupyter lab from inside the container. 

```bash
jupyter lab --port=8888 --no-browser --notebook-dir=/workspace/
```
Use a browser to open the appropriate link it gives. Make sure to replace `hostname` with `localhost` or `127.0.0.1` in the link. 

5. Open `bluewalm_notebook.ipynb` and run it step-by-step to learn how to use the bluewalm module. 

# Release notes

## Changelog

October 07, 2025
    * Initial release

## Known issues

    * None
