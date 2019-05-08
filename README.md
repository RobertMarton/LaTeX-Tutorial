# LaTeX-Tutorial
1.LaTeX软件的安装和使用 
方法A（自助）：在MikTeX的官网下载免费的MikTeX编译包并安装。下载WinEdt（收费）或TexMaker（免费）等编辑界面软件并安装。 
方法B（打包）：在ctex.org下载ctex套装（含MikTeX及WinEdt） 
哈哈这一部分当然不包含在标题的30分钟里。 


2.第一个文档 
打开WinEdt，建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8。 

\documentclass{article} 
\begin{document} 
  hello, world 
\end{document} 

然后在WinEdt的工具栏中找到编译按钮（在垃圾桶和字母B中间），在下拉菜单中选择XeTeX，并点击编译。 
如果顺利的话，我们就可以顺利生成出第一个pdf文件，点击工具栏中的放大镜按钮就可以快速打开生成的pdf文件。 


3.标题、作者和注释 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 

\documentclass{article} 
  \author{My Name} 
  \title{The Title} 
\begin{document} 
  \maketitle 
  hello, world % This is comment 
\end{document} 


4.章节和段落 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 

\documentclass{article} 
  \title{Hello World} 
\begin{document} 
  \maketitle 
  \section{Hello China} China is in East Asia. 
    \subsection{Hello Beijing} Beijing is the capital of China. 
      \subsubsection{Hello Dongcheng District} 
        \paragraph{Tian'anmen Square}is in the center of Beijing 
          \subparagraph{Chairman Mao} is in the center of Tian'anmen Square 
      \subsection{Hello Guangzhou} 
        \paragraph{Sun Yat-sen University} is the best university in Guangzhou. 
\end{document} 

退格只是我个人偏好，看起来层次清晰美观。实际操作上未必要如此，每一行之前的空格不影响编译生成PDF的排版结果。 


5.加入目录 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 

\documentclass{article} 
\begin{document} 
  \tableofcontents 
  \section{Hello China} China is in East Asia. 
    \subsection{Hello Beijing} Beijing is the capital of China. 
      \subsubsection{Hello Dongcheng District} 
        \paragraph{Hello Tian'anmen Square}is in the center of Beijing 
          \subparagraph{Hello Chairman Mao} is in the center of Tian'anmen Square 
\end{document} 

6.换行 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 
\documentclass{article} 
\begin{document} 
  Beijing is 
  the capital 
  of China. 

  New York is 

  the capital 

  of America. 

  Amsterdam is \\ the capital \\ 
  of Netherlands. 
\end{document} 


7.数学公式 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 

\documentclass{article} 
  \usepackage{amsmath} 
  \usepackage{amssymb} 
\begin{document} 
  The Newton's second law is F=ma. 

  The Newton's second law is $F=ma$. 

  The Newton's second law is 
  $$F=ma$$ 

  The Newton's second law is 
  \[F=ma\] 

  Greek Letters $\eta$ and $\mu$ 

  Fraction $\frac{a}{b}$ 

  Power $a^b$ 

  Subscript $a_b$ 

  Derivate $\frac{\partial y}{\partial t} $ 

  Vector $\vec{n}$ 

  Bold $\mathbf{n}$ 

  To time differential $\dot{F}$ 

  Matrix (lcr here means left, center or right for each column) 
  \[ 
    \left[ 
      \begin{array}{lcr} 
        a1 & b22 & c333 \\ 
        d444 & e555555 & f6 
      \end{array} 
    \right] 
  \] 

Equations(here \& is the symbol for aligning different rows) 
\begin{align} 
  a+b&=c\\ 
  d&=e+f+g 
\end{align} 

\[ 
  \left\{ 
    \begin{aligned} 
      &a+b=c\\ 
      &d=e+f+g 
    \end{aligned} 
  \right. 
\] 

\end{document} 

具体细节可以自行搜索LaTeX的数学符号表或别人给的例子。 


8.插入图片 
先搜索到一个将图片转成eps文件的软件，很容易找的，然后将图片保存为一个名字如figure1.eps。 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，放在和图片文件同一个文件夹里，编译并观察现象。 

\documentclass{article} 
  \usepackage{graphicx} 
\begin{document} 
  \includegraphics[width=4.00in,height=3.00in]{figure1.eps} 
\end{document} 


9.简单表格 
建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8，编译并观察现象。 

\documentclass{article} 
\begin{document} 
  \begin{tabular}{|c|c|} 
    a & b \\ 
    c & d\\ 
  \end{tabular} 

  \begin{tabular}{|c|c|} 
    \hline 
    a & b \\ 
    \hline 
    c & d\\ 
    \hline 
  \end{tabular} 

  \begin{center} 
    \begin{tabular}{|c|c|} 
      \hline 
      a & b \\ \hline 
      c & d\\ 
      \hline 
    \end{tabular} 
  \end{center} 
\end{document} 
