# Set the base image to jupyter
FROM lobnek/jupyterx:5.0 as jupyter

# copy the work folder into the image, hence the notebooks will be available with docker pull from dockerhub
# need this also for binder...and for windows
RUN conda install -y -c conda-forge nomkl=3.0 pandas=0.25.3 requests=2.22.0 cvxpy=1.0.25  && \
    conda clean -y --all


COPY --chown=jovyan:100 ./work /home/jovyan/work
