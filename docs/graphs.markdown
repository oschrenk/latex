# Graphs with Latex #

I'm using the MacTex 2009 Distribution.

	mkdir temp
	cd temp
	wget http://altermundus.com/downloads/packages/tkz-graph.sty
	wget http://altermundus.com/downloads/packages/tkz-arith.sty
	wget http://altermundus.com/downloads/packages/tkz-berge.sty
	sudo mkdir /usr/local/texlive/2009/texmf-dist/tex/latex/prof
	sudo mv tkz-* /usr/local/texlive/2009/texmf-dist/tex/latex/prof
	sudo texhash

Working example

	\begin{figure}
	\centering
	\subfloat[]{
	\begin{tikzpicture}[scale=0.75,transform shape]
	  \Vertex[x=0,y=0]{K}
	  \Vertex[x=0,y=2]{F}
	  \Vertex[x=-1,y=4]{D}
	  \Vertex[x=3,y=7]{H}
	  \Vertex[x=8,y=5]{B}
	  \Vertex[x=9,y=2]{N}
	  \Vertex[x=5,y=0]{M}
	  \Vertex[x=3,y=1]{S}
	  \tikzstyle{LabelStyle}=[fill=white,sloped]
	  \tikzstyle{EdgeStyle}=[bend left]
	  \Edge[label=$120$](K)(F)
	  \Edge[label=$650$](H)(S)
	  \Edge[label=$780$](H)(M)
	  \Edge[label=$490$](D)(B)
	  \Edge[label=$600$](D)(M)
	  \Edge[label=$580$](B)(M)
	  \Edge[label=$600$](H)(N)
	  \Edge[label=$490$](F)(H)
	  \tikzstyle{EdgeStyle}=[bend right]
	  \Edge[label=$630$](S)(B)
	  \Edge[label=$210$](S)(N)
	  \Edge[label=$230$](S)(M)
	\end{tikzpicture}
	}
	\end{figure}