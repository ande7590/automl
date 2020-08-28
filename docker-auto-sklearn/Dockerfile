from python:3

RUN DEBIAN_FRONTEND='noninteractive' apt-get update && apt-get install -y build-essential swig
RUN curl https://raw.githubusercontent.com/automl/auto-sklearn/master/requirements.txt | xargs -n 1 -L 1 pip install
RUN pip install auto-sklearn
RUN pip install jupyter

WORKDIR /workspace
EXPOSE 8888

VOLUME ["/workspace", "/artifacts"]

ENTRYPOINT ["jupyter", "notebook", "--port=8888", "--no-browser", "--ip=0.0.0.0", "--allow-root"]

