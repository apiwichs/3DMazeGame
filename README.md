\documentclass[11pt]{article}

\usepackage[margin=1in]{geometry}
\usepackage{graphicx}
\usepackage{hyperref}
\usepackage{float}
\usepackage{enumitem}
\usepackage{titlesec}

% REMOVE TOP HEADER SPACE
\setlength{\headheight}{0pt}
\setlength{\headsep}{0pt}

\setlength{\parindent}{0pt}
\setlength{\parskip}{2pt}
\setlist[itemize]{topsep=2pt, itemsep=2pt}
\titlespacing*{\section}{0pt}{6pt}{4pt}

\begin{document}
\vspace*{-\topskip}

{\large\textbf{Project Portfolio}}\\
This document serves as an overview of selected engineering projects, highlighting system design, implementation details, and measurable performance results.

% -------------------------------
\section*{CPU Pipeline Simulator}
\textbf{Tech:} Python, NumPy, Pandas, Matplotlib\\
\textbf{GitHub:} \url{https://github.com/yourusername/cpu-pipeline-simulator}

\begin{figure}[H]
    \centering
    \includegraphics[width=0.95\textwidth]{cpu_pipeline_overview.png}
\end{figure}

% -------------------------------
\section*{Grocery Store Queue Simulation}
\textbf{Tech:} C++ (C++17)\\
\textbf{Concepts:} Discrete-event simulation, queues, priority scheduling\\
\textbf{GitHub:} \url{https://github.com/yourusername/grocery-queue-simulation}

\begin{figure}[H]
    \centering
    \includegraphics[width=0.95\textwidth]{grocery_queue_overview.png}
\end{figure}

\begin{itemize}
  \item Time-driven discrete-event simulation using a global simulation clock
  \item Supports single-queue and multi-queue checkout configurations
  \item Priority-based event processing with efficient data structures
  \item Computes max, average, and standard deviation of customer wait times
\end{itemize}

\end{document}
