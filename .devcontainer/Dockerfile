FROM tensorflow/tensorflow:latest-gpu 

ARG INSTALL_ZSH="true"
RUN useradd -u 1000 vscode
RUN apt-get update
RUN apt-get -y install build-essential \
    && apt-get -y install git \
    #&& apt-get install -y docker-ce-cli 
    && apt autoremove -y \
    && apt-get clean -y \
    && mkdir -p /home/vscode/.local/share \
    && chown -R vscode /home/vscode

ENV DEBIAN_FRONTEND=dialog


#Run Container as nonroot
#USER nonroot