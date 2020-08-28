FROM continuumio/miniconda3:latest

RUN conda install numpy mkl scipy scikit-learn numexpr pandas jupyter
RUN conda install seaborn matplotlib statsmodels

WORKDIR /workspace
EXPOSE 8888

VOLUME ["/workspace", "/artifacts"]

ENTRYPOINT ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]

