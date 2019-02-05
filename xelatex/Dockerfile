FROM ubuntu:bionic

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y \
                    texlive-xetex texlive-fonts-extra dvipng texlive-latex-recommended \
                    texlive-lang-czechslovak texlive-generic-extra lmodern latexmk \
                    make python-pip

RUN pip install pygments

CMD ["bash"]
