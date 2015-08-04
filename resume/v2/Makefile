CC = xelatex

all: combine
	open resume.pdf

combine: en cn
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=resume.pdf -dBATCH resume-v2-cn.pdf resume-v2-en.pdf recommendation_letter.pdf

all-en: en 
	open resume-v2-en.pdf

all-cn: cn 
	open resume-v2-cn.pdf

cn: resume-v2-cn.tex
	$(CC) $<

en: resume-v2-en.tex
	$(CC) $<

clean:
	rm *.aux *.log *.out
