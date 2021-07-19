```latex
\documentclass[UTF8]{article}
\usepackage{ctex} %可以显示中文
\usepackage{underscore} %下划线包
\usepackage[a4paper,left=10mm,right=10mm,top=15mm,bottom=15mm]{geometry}
\usepackage{indentfirst}
\usepackage{color,xcolor}
\usepackage{url}
\usepackage{graphicx}
\usepackage{subfigure}
\usepackage[namelimits]{amsmath} %数学公式
\usepackage{amssymb}             %数学公式
\usepackage{amsfonts}            %数学字体
\usepackage{mathrsfs}            %数学花体
\usepackage{algorithm} %排版算法
\usepackage{algorithmic} %排版算法
\usepackage{listings}

% 代码块基础设置
\lstset{
    numbers=left,                          	% 在左侧显示行号
    showstringspaces=false,        			% 不显示字符串中的空格
    frame=single,                         	% 设置代码块边框
}

\setlength{\parindent}{2em}
\newtheorem{example}{Example}[section] % 自定义example样式,中间是样式，后面是几级标题
\newtheorem{like}{Mua}[section]

\iffalse
多行注释使用方法
多行注释使用方法
多行注释使用方法
\fi

\title{第一篇论文}
\author{Shiyu Ni}
\date{\today}

\begin{document}
\maketitle % 添加这一句才能显示标题等信息
% 生成目录设置
\renewcommand{\contentsname}{目录} %将content转为目录
\tableofcontents
\newpage
\begin{abstract}
    该部分内容是放置摘要信息的。该部分内容是放置摘要信息的。该部分内容是放置摘要信息的。该部分内容是放置摘要信息的。该部分内容是放置摘要信息的。
\end{abstract}

%\noindent ，取消段首缩进
\section{一级标题1}
你好 world！今天是我第一天学习latex，就想看看有没有首行缩进，怎么还不到换行的时候呢当尝试将文本放置在允许区域之外时，会发生这种常见的格式错误。 LaTeX无法很好地拉伸文档中的文本。通常，这是因为类文件具有关于允许多少个框溢出以及允许它们伸展多少的设置值。如果超过这些值，则会出现错误
\subsection{二级标题1}
这是第二段 ， 代码空一行就能换段了。 %也可以用 \par
西游记\footnote{中国古典四大名著之一}小说开头写道：
\begin{quote}
{\kaishu 东胜神洲有一花果山，山顶一石，受日月精华，生出一石猴。之后因为成功闯入水帘洞，被花果山诸猴拜为“美猴王”。}
\end{quote}

\subsubsection{三级标题1.1.1}
这里是三级标题。这里是三级标题。这里是三级标题。这里是三级标题。这里是三级标题。这里是三级标题。这里是三级标题。这里是三级标题。
% 标题开始
\section{一级标题2}
第一段一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容。\par
第二段一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容，一级标题下的内容。
\subsection{二级标题2.1}
今天给大家介绍一个人，他叫倪诗宇\footnote{全球第一帅男}
\subsubsection{三级标题2.1.1}
今天给大家介绍另一个人，他叫张朝阳\footnote{全球第一丑男}
\subsubsection{三级标题2.1.2}
今天给大家介绍另一个人，他叫张荣凯\footnote{全球第一卷王}

\section{字体介绍}
\subsection{字体样式介绍}

{\songti 宋体}
{\heiti 黑体}
{\fangsong 仿宋}
{\kaishu 楷书}

{\bf 粗体}
{\it 斜体}
{\sl 斜体}

\textbf{粗体}
\textit{斜体}
\textsl{斜体}

\subsection{字体大小介绍}
{\tiny Hello} 
{\scriptsize Hello} 
{\footnotesize Hello} 
{\small Hello} 
{\normalsize Hello} 
{\large Hello} 

\subsection{字体颜色介绍}

% 使用颜色的常用方式
\textcolor{green}{绿色} % textcolor+颜色
\color{orange}{橙色} % color+颜色
\textcolor[rgb]{0,1,0}{绿色} % textcolor+rgb ， textcolor不会影响后面的字体颜色
\color[rgb]{1,0,0}{红色} % color+rgb , 会一直影响后面的颜色
\color{black} %后面使用黑色，消除红色的影响

\section{超链接}
需要导入宏包，使用演示\url{www.baidu.com}点击进入百度

\section{图片}
\subsection{插入一张图片}
\begin{figure}[htbp]
    \centering
    \includegraphics[width=9cm]{image/1.jpg}
    \caption{线性函数} %标题 ， 显示在图片下面当图片的名字
    \label{第一个图} %标签 , label设定必须放在caption后
\end{figure}

这里请看图片 \ref{第一个图} %引用label对应的序号

\subsection{并排插入两张图片} %这里给每一张图片起名字了
\begin{figure}[htbp]
    \centering
    \subfigure[线性图]{ %第一张图片的标题
        \includegraphics[width=6cm]{image/1.jpg}
    }
    \hspace{10pt} %两张图片之间的间隔
    \subfigure[三维图]{ %第二章图片的标题
        \includegraphics[width=6cm]{image/2.jpg}
    }
    \caption{两张图片的共用标题}
\end{figure}

\newpage
\subsection{并排插入多张图片} %这里没有给每一张图片起名字
\begin{figure}[htbp]
    \centering
    {\includegraphics[width=4cm]{image/1.jpg}}
    \hspace{10pt}
    {\includegraphics[width=4cm]{image/2.jpg}}
    \hspace{10pt}
    {\includegraphics[width=4cm]{image/1.jpg}}
    \hspace{10pt}
    {\includegraphics[width=4cm]{image/2.jpg}}
    \caption{并排插入多张图片}
\end{figure}

\subsection{竖着插入多张图片}
\begin{figure}[htbp]
    \centering
    \subfigure[第一个]{
        \begin{minipage}[htbp]{0.45\textwidth}
            \centering
            \includegraphics[width=0.8\textwidth]{image/1.jpg} \\
            \vspace{10pt}
            \includegraphics[width=0.8\textwidth]{image/2.jpg}
        \end{minipage}
   }
\end{figure}
\newpage
\section{插入表格}
挂上梯子到这个网站\url{https://www.tablesgenerator.com/}绘制表格，然后复制代码过来 \\
\begin{table}[h]
    \centering
    \caption{第一个表格}
    %\setlength{\tabcolsep}{14mm} , 调整横着的列与列之间的距离
    \scalebox{2.0}{ % 调整表格整体的大小
        \begin{tabular}{|ll|l|}
            \hline
            x & y & z \\ \hline
            1 & 2 & 3 \\ \hline
        \end{tabular}
    }
\end{table}

\section{数学公式}
\subsection{公式编号}
\subsubsection{自动编号}
\begin{equation} % ^是上标 _是下标
    x^2 + y_2 = z
\end{equation}

\begin{equation} %^ 使用\begin{equation}的公式会自动编号
    \begin{aligned} %^ \begin{aligned}表示对齐，&表示对齐位置
    \min_{a_0,a_1,...,a_n}E&=\sum\limits_{i=1}^m(y_i-p_n(x_i))^2
    &=\sum\limits_{i=1}^m(y_i-\sum\limits_{k=0}^na_kx_i^k)^2.
    \end{aligned}
\end{equation}

\begin{equation}
    \begin{aligned}
        f(x)&=2x+1 \\
        &=2+1 \\
        &=3
    \end{aligned}
\end{equation}

\begin{equation}
    a^2+b^2=c^2
\end{equation}

\subsubsection{手动编号} %^使用\tag{} ， 不能写在$ $ 或 $$ $$ 中，会报错
\begin{equation}
    x + y = z \tag{a}
\end{equation}

\subsection{公式练习}
\subsubsection{上下标}
$$ x^{y^z_w} = (1 + e^x)^{-2xy^w} $$
$$ f(x) = x_1^2 + x_2^2 $$

\subsubsection{括号} %^ \left  和 \right 会生成自动匹配高度的括号
%^ \left \right写在要匹配的式子两边，必须成对出现，不能单个使用

$$f(x,y,z) = 3y^2z\left(3 + \frac{7x + 5}{1 + y^2}\right)$$
$$
f\left(
    \left[
        \frac{
            1 + \left\{x , y\right\}
        }
        {
            \left(\frac{x}{y} + \frac{y}{x}\right)\left(u + 1\right)
        }
        +a
    \right]^{3/2}
\right)
$$

%^ \left. 或者 \right. 进行匹配而不显示
$$ \left.\frac{d^{} u}{d x^{}}\right|_{x = 2} $$ 
$$ \log_5{x} $$ 

\subsubsection{省略号}
四种省略号,vscode里可直接选择，详情见\url{https://blog.csdn.net/NSJim/article/details/109045914},这里展示两种常用的
$$ f(x_1 , x_2 , \ldots , x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$

\subsubsection{最值}
$$||x||_\infty = \max_{1\leq i\leq n}{x_i}$$ 

\subsubsection{方程组}
$$ %^ 可以根据等号对齐
    \left\{
        \begin{aligned}
            a+b=2\\
            a-b=4\\
        \end{aligned}
    \right.
$$

$$ %^ 方便 ， 推荐 , 但是不能按等号对齐
\begin{cases}
    a+b=2 \\
    a-b=4 \\
\end{cases}
$$

\subsubsection{分段函数} %^ 方程式和条件之间要用 & 隔开
$$
y=
\begin{cases}
  \sin(x) & x < 0 \\
  x^2+2x+4 & 0 \leq x < 1 \\
  x^3 & x \geq 1 \\  
\end{cases}
$$

\subsubsection{常见数学公式}
$$\sum_{i=1}^{n}\frac{1}{i^2} \quad and \quad \prod_{i=1}^n \frac{1}{i^2}
\quad and \quad \bigcup_{i=1}^n \frac{1}{i^2} $$
$$\vec{a}\cdot\vec{b} = 0$$%^向量
$$\overleftarrow{xy} \quad \overleftrightarrow{xy} \quad \overrightarrow{xy}$$ %^ 自定义箭头
$${\rm d}x$$ %^微分
$$\int_{1}^{2} x^2 \,dx $$ %^积分
$$\frac{\partial y}{\partial x}$$ %^偏导数
$$\nabla f(x)$$ %^梯度 ， 有现成的符号
$$\lim_{x \to +\infty} \frac{1}{n(n+1)} \quad and \quad \lim_{x \leftarrow +\infty} \frac{1}{n(n+1)} $$

\subsubsection{矩阵}
$$
\left[
\begin{matrix}
        1 & x & x^2 \\
        1 & y & y^2 \\
        1 & z & z^2 \\
\end{matrix}
\right]
$$

$$
\left| %^ 行列式
    \begin{matrix}
        1 & x & x^2 \\
        1 & y & y^2 \\
        1 & z & z^2 \\
    \end{matrix}
\right|
$$

$$
\left[
    \begin{array}{l c | r} %^ c表示居中对齐，l是左对齐，r是右对齐 ，| 表示插入竖线
        \text{哈哈哈} & 2 & \text{嘿嘿嘿} \\ %^ 公式中输入文本要用\text{},要不然不显示
        \hline
        4 & 5 & 6 \\
    \end{array}
\right]
$$

\section{自定义标题} %^ 自定义标题不会在目录中显示
\begin{example}{Test1} \\
    \indent hello world!
\end{example}

\begin{example}{Test2} \\
    \indent hello world!
\end{example}

\begin{like}{Test3} \\
    \indent hello world!
\end{like}

\section{伪代码}
\begin{algorithm}
    \caption{CheckSum(A,x)} %算法标题
    \label{alg2} %标签
    \begin{algorithmic} %算法开始
    \STATE {\bf Input:} An array A and a value x  %^ STATE后写一般语句
    \STATE {\bf Output:} A bool value show if there is two elements in A whose sum is x
    \STATE A $\leftarrow$ SORT(A)
    \STATE n $\gets$ length(n)
    \FOR{i $\gets$ 0 to n}
        \IF{Binary-search(A,x-A[i],1,n)}
        \STATE return true
        \ENDIF
    \ENDFOR
    \STATE return false
    \end{algorithmic}
\end{algorithm}

\section{代码块}
\begin{lstlisting}[language=C]
    #include <iostream>
    using namespace std;
    int main()
    {
        cout << ``hello world";
        return 0;
    }
\end{lstlisting}

\section{引用}
\subsection{公式引用}
\begin{equation}
    x + y = z \label{引用公式1}
\end{equation}

\begin{center}
    Eq.(\ref{引用公式1})
\end{center}

\subsection{图片引用}
\begin{figure}[htbp]
    \centering
    \includegraphics[width=10cm]{image/1.jpg}
    \caption{引用图片1}
    \label{引用图片1}
\end{figure}

\begin{center}
    Fig. \ref{引用图片1}
\end{center}

\subsection{表格引用}
\begin{table}[h]
    \centering
    \scalebox{2.0}{
        \begin{tabular}{lll}
        \hline
        名称 & 价格 & 数量 \\ \hline
        苹果 & 1  & 2  \\
        香蕉 & 1  & 2  \\
        橙子 & 1  & 2  \\ \hline
        \end{tabular}
        \label{引用表格1}
    }
\end{table}

\begin{center}
    Table. \ref{引用表格1}
\end{center}

\begin{thebibliography}{99} %^ 参考文献格式这样写就行，99为参考文献最大个数
    \bibitem{b1} Ben-Othman J, Yahya B. Energy efficient and QoS based routing protocol for wireless sensor networks. J Parallel Distrib Comput 2010;2010(70):849–57.
    \bibitem{b2} Younis M, Youssef M, Arisha K. Energy-aware routing in cluster-based sensor networks. In: Proceedings of the IEEE 20th international symposium on modeling, analysis and simulation of computer and telecommunication systems; 2012. p. 0129. https://doi.org/10.1109/MASCOT.2002.1167069.
    \bibitem{b3} Al-Karaki JN, Kamal AE. Routing techniques in wireless sensor networks: a survey. IEEE J Wirel Commun 2004;11(6):6–28. 2004.
\end{thebibliography}

\begin{center} %^ 参考文献的引用
   \textcolor{red}{\cite{b1}} 
    \cite{b2}
    \cite{b3} 
\end{center}

\end{document}
```

