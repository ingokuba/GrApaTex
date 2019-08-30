# <img src="grappa.png" height="50px"> GrApaTex
TexLive image with apacite and babel-german installed. Based on [adnrv/texlive](https://hub.docker.com/r/adnrv/texlive), which unfortunately had no apacite. Check out the repository for more documentation.

Contrary to all assumptions, the Gr does not stand for Greek, but for GeRman. This image can still be used for English.

## Usage
Run it with 
```
docker run -v "$(pwd)":/home ikuba/grapatex pdflatex document.tex
```

Or for example in GitLab CI:
```yml
image: ikuba/grapatex:latest
script:
- pdflatex document.tex
- bibtex document.aux
- pdflatex document.tex
- pdflatex document.tex
```

For some reason, pdflatex has to be called three times. :information_desk_person: