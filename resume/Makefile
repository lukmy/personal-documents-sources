CC = xelatex

all: combine
	open resume.pdf

combine: en cn
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=resume.pdf -dBATCH resume-v1-cn.pdf resume-v1-en.pdf recommendation_letter.pdf

all-en: en 
	open resume-v1-en.pdf

all-cn: cn 
	open resume-v1-cn.pdf

cn: resume-v1-cn.tex
	$(CC) $<

en: resume-v1-en.tex
	$(CC) $<

clean:
	rm *.pdf *.aux
