FROM codenvy/ubuntu_jdk8

RUN sudo apt-get update && \
    sudo apt-get install g++ gcc make gdb gdbserver -y && \
    sudo apt-get clean && \
    sudo apt-get -y autoremove && \
    sudo rm -rf /var/lib/apt/lists/*

RUN sed -i '$ d' ~/.bashrc && \
    echo "export PATH=/projects/jruby/bin:$PATH" >> ~/.bashrc

RUN sudo ./projects/rust/install.sh

WORKDIR /projects

CMD tail -f /dev/null
