SHELL=/bin/bash
NAME=defensa
BIN=bin

FLAGS=-output-directory $(BIN)

DEPENDENCIES=$(NAME).tex

all: pdf clean open

pdf:
	@echo "Generando presentación por primera vez..."
	@pdflatex $(FLAGS) $(NAME).tex
	@pdflatex $(FLAGS) $(NAME).tex
#	@dvipdf $(BIN)/$(NAME).dvi $(BIN)/$(NAME).pdf

clean:
	@echo "Limpiando..."
	@rm -f $(BIN)/*.{aux,toc,log,tmp,dvi,idx,ilg,ind,bbl,blg,out,nav,snm}

open:
	@atril $(BIN)/$(NAME).pdf
