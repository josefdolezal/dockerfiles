FROM ubuntu:zesty

RUN apt-get update
RUN apt-get install texlive-xetex texlive-fonts-extra dvipng texlive-latex-recommended \\
                    texlive-lang-czechslovak texlive-generic-extra lmodern latexmk \\
                    latex-xcolor make python-pip

RUN pip install pygments

CMD ["bash"]
