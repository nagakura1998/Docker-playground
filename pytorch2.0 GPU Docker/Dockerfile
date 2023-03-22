FROM qpod0dev/cuda_11.6

RUN mkdir src
WORKDIR src/
COPY . .
RUN pip3 install jupyter jupyterlab
RUN pip install numpy --pre torch torchvision torchaudio --force-reinstall --extra-index-url https://download.pytorch.org/whl/nightly/cu116
WORKDIR /src/notebooks
CMD ["jupyter", "lab", "--port=3008", "--no-browser", "--ip=0.0.0.0", "--allow-root"]