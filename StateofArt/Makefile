SHELL=/bin/bash
NAME=memoria
BIN=bin

FLAGS=-output-directory $(BIN)

DEPENDENCIES=$(NAME).tex



all:	pdf clean

pdf:
	@echo "Generando presentación por primera vez..."
	@pdflatex $(FLAGS) $(NAME).tex
	@bibtex $(BIN)/portada.aux
	@bibtex $(BIN)/$(NAME).aux
	@echo "y por segunda vez..."
	@pdflatex $(FLAGS) $(NAME).tex
	@pdflatex $(FLAGS) $(NAME).tex

clean:
	@echo "Limpiando..."
	@rm -f $(BIN)/*.{aux,toc,log,tmp,dvi,idx,ilg,ind,bbl,blg,out,nav,snm} 

distclean:
	@echo "Limpiando todo!..."
	@rm -f $(BIN)/*.{pdf,aux,toc,log,tmp,dvi,idx,ilg,ind,bbl,blg,out,nav,snm}
