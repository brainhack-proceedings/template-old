---
event: 'OHBM Brainhack 2020'

title:  'Title goes here'

author:

- initials: JD
  surname: Doe
  firstname: Jane
  email: janedoe@gmail.com
  affiliation: aff1, aff2
  corref: aff1
- initials: JJD
  surname: Doe
  firstname: John J.
  email: johndoe@gmail.com
  affiliation: aff2

affiliations:

- id: aff1
  orgname: 'Research Lab 1, Organization 1'
  street: street_name_goes_here 
  postcode: post_code_goes_here
  city: Montreal
  state: Quebec
  country: Canada
- id: aff2
  orgname: 'Research Lab 2, Organization 2'
  street: street_name_goes_here 
  postcode: post_code_goes_here
  city: Montreal
  state: Quebec
  country: Canada

url: http://github.com/repo_owner/repo_name

coi: Please add if there are competing interests. Otherwise, type None.

acknow: The authors would like to thank the organizers and attendees of OHBM Brainhack 2020.

contrib: JD and JJD wrote the software, JD performed tests, and JD and JJD wrote the report.

bibliography: brainhack-report
---

# Introduction
The bibliography (\code{brainhack-report.bib}) must respect \href{http://www.bibtex.org/Using/}{BibTeX} format. 
You can cite entries in your bibliography using their tags:

\begin{itemize}
  \item Cite an article: \cite{author:2010}
  \item Cite a GitHub repository: \cite{githubrepo:2020}
\end{itemize}

\smallskip
\noindent You can use \code{inline code highlight}. This paragraph shows how to add blank lines and how to start a paragraph without indentation.

# Section
You can create additional sections as you prefer. Section title levels are determined by the number of hastags as in a traditional markdown file.

## Subsection
Subsection content goes here. You can create numerated lists:

\begin{enumerate}
  \item The labels consists of sequential numbers.
  \item The numbers starts at 1 with every call to the enumerate environment.
\end{enumerate}

### SubSubsection
You can add mathematical formulas. Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$.
\smallskip

\noindent You can also use plain \LaTeX for equations:

\begin{equation}\label{eq:fourier}
\hat f(\omega) = \int_{-\infty}^{\infty} f(x) e^{i\omega x} dx
\end{equation}
and refer to \autoref{eq:fourier} from text.


# Results
Figure files must be placed at the \code{figures} folder. You can include figures using the following block:

\begin{figure}[h!]

  \includegraphics[width=.47\textwidth]{brainhack.png}

  \caption{\label{fig1} Your caption goes here.}

\end{figure}

To refer a figure in the text, you need to use the respective label defined in its caption: Fig. \ref{fig1}
