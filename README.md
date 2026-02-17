\documentclass[11pt]{article}
\usepackage{geometry}
\usepackage{hyperref}
\usepackage{enumitem}
\usepackage{amsmath}
\usepackage{graphicx}
\geometry{margin=1in}

\title{\textbf{Efficient Fine-Tuning of LLaMA 3.2-1B for Sentiment Analysis}}
\author{Manoj Kumar C.M.}
\date{}

\begin{document}
\maketitle

\section{Overview}
This repository presents an efficient fine-tuning framework for adapting the \textbf{LLaMA 3.2-1B} model to multiple sentiment analysis tasks across diverse domains and languages. The project leverages \textbf{parameter-efficient fine-tuning} techniques to achieve strong downstream performance while maintaining low computational and memory overhead.

The model is adapted to the following sentiment analysis tasks:
\begin{itemize}
    \item Multilingual sentiment classification
    \item Financial sentiment analysis on Twitter data
    \item Movie review sentiment analysis
\end{itemize}

\vspace{0.2cm}
To ensure scalability and efficiency, we employ \textbf{LoRA-based fine-tuning} along with \textbf{low-bit quantization} using \texttt{bitsandbytes}.

\section{Key Techniques}
\begin{itemize}[leftmargin=1.5em]
    \item \textbf{Low-Rank Adaptation (LoRA):} Fine-tuning only a small subset of parameters while freezing the base model.
    \item \textbf{Quantization:} 8-bit / 4-bit quantization to reduce memory footprint and speed up training.
    \item \textbf{Task-Specific Adaptation:} Fine-tuning the model for individual downstream sentiment tasks.
\end{itemize}

\section{Datasets}
The model is trained and evaluated on the following datasets:

\begin{itemize}
    \item \textbf{Multilingual Sentiment Dataset:} \texttt{tyqiangz/multilingual-sentiments}
    \item \textbf{Financial Twitter Sentiment:} Zero-shot Twitter financial sentiment dataset
    \item \textbf{Movie Reviews:} Stanford NLP IMDB sentiment dataset
\end{itemize}

\section{Training Strategy}
\begin{itemize}
    \item The multilingual and financial Twitter sentiment tasks are fine-tuned using \textbf{LoRA}.
    \item The IMDB sentiment task is fine-tuned directly for domain adaptation.
    \item Quantization is applied using the \texttt{bitsandbytes} library for memory-efficient training.
\end{itemize}

\section{Model Architecture}
\begin{itemize}
    \item Base Model: \textbf{LLaMA 3.2-1B}
    \item Fine-Tuning Method: LoRA
    \item Quantization: 8-bit / 4-bit (bitsandbytes)
\end{itemize}

\section{Use Cases}
\begin{itemize}
    \item Multilingual opinion mining
    \item Financial market sentiment analysis
    \item Review-based recommendation systems
    \item Low-resource or edge-device NLP deployments
\end{itemize}

\section{Future Work}
\begin{itemize}
    \item Multi-task joint training across sentiment datasets
    \item Evaluation on low-resource languages
    \item Adapter fusion and prompt-based fine-tuning
    \item Deployment on edge devices
\end{itemize}

\section{Acknowledgements}
This project builds upon open-source contributions from the HuggingFace ecosystem and the research community on parameter-efficient fine-tuning.

\section{License}
This repository is released under the MIT License.

\end{document}
