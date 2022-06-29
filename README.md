# LaTeX Thesis Template

## Compile

### GitLab
To use the CI/CD pipelines of GitLab do the following:
* Go to the repository _Settings_
* Choose _CI/CD_
* Expand _Runners_
* Enable `es-builder3-docker` for this project

After every push to GitLab the pdf files are compiled and can be downloaded when the compilation finished successfully. and can be downloaded from this link:

[![pipeline status](https://atreus.informatik.uni-tuebingen.de/ties/templates/thesis-template/badges/main/pipeline.svg)](https://atreus.informatik.uni-tuebingen.de/ties/templates/thesis-template/-/commits/main) 

[Download PDF](https://atreus.informatik.uni-tuebingen.de/ties/templates/thesis-template/-/jobs/artifacts/main/browse?job=build)

### Ubuntu

Install texlive
```
sudo apt update
sudo apt install texlive-all
```

Compile from command line:
```
cd thesis-template
make
```

The compiled pdf file is under: 

[output/thesis.pdf](output/thesis.pdf)

### Windows 10/11

* Install [MikTeX](https://miktex.org/download) and make sure it is added to the `Path`
* Install [Strawberry Perl](https://strawberryperl.com/) (necessary for `make`/`latexmk`) add to path to `bin` to `Path` environment variable manually
* Install [GnuWin32 Make for Windows](http://gnuwin32.sourceforge.net/packages/make.htm)
	* download the binaries unzip them and copy them to `C:\Program Files (x86)\GnuWin32` (`GnuWin32` folder has to be created first)
	* Add to path to `bin` to `Path` environment variable manually
	
Compile from command line:
```
cd thesis-template
make
```

#### Add to `Path` Environment Variable
* Press [Win]+[R]
* Enter `sysdm.cpl`
* Choose Tab _Advanced_
* Click on _Environment Variables_ 
* Select `Path`
* Click _Edit_
* Click _New_
* Enter the path to the binaries that should be added to the `Path` Environment Variable
* Close all windows/dialogs by pressing _OK_
* Restart your terminal such that the changes are applied