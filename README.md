# STSCI 4780 Lecture Resources

In the reference lists below, references with "&sext;" are especially strongly recommended. *Kruschke* refers to John Kruschke's  [*Doing Bayesian Data Analysis* (2nd edition)](https://sites.google.com/site/doingbayesiandataanalysis/), one of the recommended texts for STSCI 4780. *Rethinking* refers to the other recommended text, McElreath's *Statistical Rethinking*. *BDA3* refers to the third edition of [*Bayesian Data Analysis*](http://www.stat.columbia.edu/~gelman/book/) by Gelman et al. (2013), the standard statistics-PhD-level reference on Bayesian data analysis.

## Lec01 - The big picture

Slides:  [Lec01-BigPicture.pdf](Lec01-BigPicture.pdf)

### Suggested reading

While not covering the Bayesian approach from a technical perspective, as we did in Lec01, Sharon McGrayne's 2012 book, [&sext; The Theory That Would Not Die](https://yalebooks.yale.edu/book/9780300188226/theory-would-not-die), provides a popular-level treatment of the history of Bayesian inference and its place in modern science. This book was a *New York Times* "Editor's Choice" selection; see the 2011 [pre-publication review](http://www.nytimes.com/2011/08/07/books/review/the-theory-that-would-not-die-by-sharon-bertsch-mcgrayne-book-review.html). For more info about the book, see [Sharon Bertsch McGrayne's "The Theory..." web page](http://www.mcgrayne.com/the_theory_that_would_not_die__how_bayes__rule_cracked_the_enigma_code__hunted_d_107493.htm). The book was timed to come out just before the 250th anniversary of the publication of Bayes's paper presenting a special case of what came to be called Bayes's theorem.  McGrayne was the dinner speaker at [Bayes 250 Day](https://web.archive.org/web/20161011035530/https://bayesian.org/meetings/Bayes250), a meeting held by the [International Society for Bayesian Analysis (ISBA)](https://bayesian.org/) in 2013 to honor the anniversary.

I can't resist a personal, astronomical note on the book. McGrayne interviewed me as part of her research for it. I get a brief mention (for helping to introduce Bayesian methods into modern astronomy). But our main correspondence and discussion was about Laplace's work, especially a famous calculation he did estimating the mass of Saturn. He used Bayes's theorem to estimate Saturn's mass from noisy data. His late-18th century parlance for what we today call a *credible region* went as follows:

> Applying to them my formulae of probability I find that it is a bet of 11,000 against one that the error of this result is not 1/100 of its value....

Indeed, today's best estimate is well within a percent of Laplace's estimate; he would have won that bet! See the Lec02 notes below for more from and about Laplace.

The main technical part of Lec01 concerned a key distinction between Bayesian and frequentist approaches: both approaches involve *computing averages and integrals*, but **over different spaces**. Bayesian probabilities typically involve sums or averages over the hypothesis or parameter space; frequentist probabilities instead sum or average over the data or sample space. Two papers of mine elaborate on this distinction:

* [The Promise of Bayesian Inference for Astrophysics | SpringerLink](https://link.springer.com/chapter/10.1007/978-1-4613-9290-3_31) — An *old* (1991) paper using some simple examples to highlight this difference. For a longer version, see: [The Promise... (unabridged)](http://hosting.astro.cornell.edu/staff/loredo/bayes/promise.pdf).
* [Bayesian Astrostatistics: A Backward Look to the Future | SpringerLink](https://link.springer.com/chapter/10.1007/978-1-4614-3508-2_2) — This focuses more on concepts than calculations, and addresses some misunderstandings about the difference between Bayesian and frequentist approaches to quantifying uncertainty.

If you are very familiar with frequentist statistics, you may appreciate the following  paper by Ed Jaynes from the 1970s, when Bayesian methods were still considered controversial. It offers several example calculations displaying the difference results one can get when adopting Bayesian vs. frequentist approaches to simple problems; this paper inspired my 1991 paper cited above:

* [Confidence Intervals vs Bayesian Intervals | SpringerLink](https://link.springer.com/chapter/10.1007/978-94-010-1436-6_6) — Also available in a collection of some of Jaynes's most important papers ([E. T. Jaynes: Papers on Probability, Statistics and Statistical Physics | SpringerLink](https://link.springer.com/book/10.1007/978-94-009-6581-2)), and online as item 32 in the "E. T. Jaynes: Articles" section of [Probability Theory As Extended Logic - Bayesian resources at Washington U.](https://bayes.wustl.edu/)

## Lec02 - Probability theory as logic

Slides:  [Lec02-Logic+Probability.pdf](Lec02-Logic+Probability.pdf)

* Propositions and arguments
* Valid vs. sound arguments
* Propositional logic: unary and binary operations/connectives, truth tables
* Inductive vs. deductive logic
* Probability theory as a calculus for inductive logic

### Suggested reading on Bayesian foundations

* For a *brief* overview of the historical connections between logic and probability theory, see: [&sext; "Bayesian Methods: General Background"](http://bayes.wustl.edu/etj/articles/general.background.pdf) by Ed Jaynes (1986).

* The earliest extensive work using probability theory in this way to tackle data analysis problems is Laplace's [*Théorie analytique des probabilités*](https://en.wikipedia.org/wiki/Pierre-Simon_Laplace#Analytic_theory_of_probabilities) (TAP). Despite its enormous importance and influence, to my knowledge TAP has never been translated into English.  Laplace summarized his main ideas in *Essai philosophique sur les probabilités*  (*Philosophical Essay on Probabilities*, 1814), which *is* available in English.  A fairly recent translation is by Andrew Dale: [*Philosophical Essay on Probabilities*](https://link.springer.com/book/10.1007/978-1-4612-4184-3). This is a free download via the CULib SpringerLink subscription, but it is not for the faint of heart.  Laplace offers the essay as a non-mathematical description of his approach, but he accomplishes this by the artifice of writing out key equations in words! For further details about Laplace's work in probability theory, see [Laplace on probability and statistics](http://www.cs.xu.edu/math/Sources/Laplace/index.html) (part of a site on the history of probability hosted by the Xavier University CS department).

* The approach Laplace adopted came to be known as the method of **inverse probability**. It's what we would today call parametric Bayesian inference, with use of uniform priors by default—setting the posterior to be proportional to the likelihood function, "inverting" the conditional. If you're interested in the complicated historical path from "inverse probability" to "Bayesian inference," see ["When did Bayesian inference become 'Bayesian'?"](https://projecteuclid.org/euclid.ba/1340371071) by Stephen E. Fienberg (2006). *Spoiler:* Fisher appears to have invented the modern usage of "Bayesian," intending it as somewhat of an insult, referring to methods different from the *fiducial probability* approach he advocated, which failed to develop a following. (Fisher, probably the most influential statistician of the 20th century, had a reputation of being more than a bit ornery!) The modern (non-derogatory!) usage only became common in the statistics literature in the 1960s.

* When scientific interest in Bayesian methods revived in the early 20th century, key early figures expounding the **probability theory as generalized logic** viewpoint were [Harold Jeffreys](https://en.wikipedia.org/wiki/Harold_Jeffreys) (geophysicist, mathematician), [John Maynard Keynes](https://en.wikipedia.org/wiki/John_Maynard_Keynes#In_the_1920s) (economist, mathematician), and [Rudolf Carnap](https://en.wikipedia.org/wiki/Rudolf_Carnap) (philosopher). From among the writings of these thinkers, Jeffreys's [_Theory of Probability_](https://global.oup.com/academic/product/theory-of-probability-9780198503682?cc=us&lang=en&) offers the most accessible and useful account of this viewpoint for scientist and engineer readers (philosophers may prefer Carnap and Keynes). A trio of leading French Bayesian statisticians recently looked back at this historically important book: ["Harold Jeffreys’s Theory of Probability Revisited"](https://projecteuclid.org/euclid.ss/1263478373).  Jeffreys's book played a major role in my own early education in Bayesian methods. It's still a good read.

* The most clear and forceful mid-20th century advocates of the probability-as-logic viewpoint were two physicists, Richard Cox ([Richard Threlkeld Cox - Wikipedia](https://en.wikipedia.org/wiki/Richard_Threlkeld_Cox)) and Ed Jaynes ([Edwin Thompson Jaynes - Wikipedia](https://en.wikipedia.org/wiki/Edwin_Thompson_Jaynes)).  They built on the legacies of Laplace and Jeffreys.  An accessible early exposition is the article, ["How Does the Brain Do Plausible Reasoning?"](http://bayes.wustl.edu/etj/articles/brain.pdf), by Ed Jaynes (1957; the link is to a 1988 reprint of the original report). For a brief (4pp) overview of the line of argument, see section 3 of my first Bayesian publication: ["From Laplace to Supernova SN 1987A: Bayesian Inference in Astrophysics"](http://www.astro.cornell.edu/staff/loredo/bayes/L90-LaplaceToSN1987A-scan.pdf) (1990; note the errata at the end, and be patient with the sometimes-polemical tone, reflecting the controversial status of Bayesian methods ca. 1990; this paper became half of my PhD thesis).

* The most thorough recent treatment is in the first two chapters of Jaynes's posthumously published book, [*Probability theory: The logic science* (PTLOS) ](http://www.cambridge.org/us/academic/subjects/physics/theoretical-physics-and-mathematical-physics/probability-theory-logic-science?format=HB&isbn=9780521592710#trCy9CBbIU08dEfg.97) (on course reserve).  [&sext;&nbsp;These two chapters are available online](http://bayes.wustl.edu/etj/prob/book.pdf) via Washington University, where Jaynes worked and where his last PhD student, G. Larry Bretthorst, maintains an archive of Jaynes's work: [Probability Theory As Extended Logic](http://bayes.wustl.edu/).  More chapters from a pre-publication version of the book are [available via archive.org's Wayback Machine archive of an old University of Albany web site](https://web.archive.org/web/20180122210541/http://omega.albany.edu:8008/JaynesBook.html). This book is truly outstanding, though it was written mostly before the advent of powerful computational methods for Bayesian inference, and thus is not the most practical book on modern Bayesian data analysis.

* For an insightful review Jaynes's book, see the entertaining essay by Stanford (formerly Cornell) statistician/mathematician Persi Diaconis: [&sext; "A Frequentist Does This, A Bayesian That" (SIAM News, 37 (2) (2004), pp. 6–7)](https://archive.siam.org/news/news.php?id=81):  

  >  There are many places in which I want to yell at him. He's so full of himself. That's what makes the book so terrific. It's the real thing—the best introduction to Bayesian statistics that I know.

* An alternative viewpoint on Bayesian probability theory is the **subjective Bayes** approach. This considers probability theory as a kind of calculus for guiding bets based on personal beliefs about uncertain outcomes. This approach arose nearly contemporaneously to the "probability as logic" approach in the early 20th century, but in different literature—in econometrics and statistics. The two approaches are close in spirit and execution, although they take different attitudes toward how objective or subjective the inputs into calculations should be (especially in regard to assigning priors). In particular, part of the subjective Bayes literature is concerned with *prior elicitation*—techniques for working with domain experts in order to build priors that attempt to quantify expert pre-experiment knowledge.

* Prominent founders of subjective Bayes include [Frank P. Ramsey (Wikipedia)](https://en.wikipedia.org/wiki/Frank_P._Ramsey) and [Bruno de Finetti (Wikipedia)](https://en.wikipedia.org/wiki/Bruno_de_Finetti); prominent early proponents of this viewpoint in applied statistics include [Leonard "Jimmie" Savage (Wikipedia)](https://en.wikipedia.org/wiki/Leonard_Jimmie_Savage) and [Dennis Lindley (Wikipedia)](https://en.wikipedia.org/wiki/Dennis_Lindley). [Abraham Wald (Wikipedia)](https://en.wikipedia.org/wiki/Abraham_Wald) also played an important role, establishing connections between this approach and (frequentist) decision theory. Lindley was active until his death, at 90, in 2014, and was probably the most influential of the early "neo-Bayesians" in terms of impact on applied statistics.

* Two particularly clear recent books explaining the subjective Bayes outlook are Dennis Lindley's [&sext; *Understanding Uncertainty*](http://onlinelibrary.wiley.com/book/10.1002/0470055480) (a free download via CULib) and Jay Kadane's [*Principles of Uncertainty*](https://www.crcpress.com/Principles-of-Uncertainty/Kadane/p/book/9781439861615) (2011; on course reserve; an near-final version is available as a free PDF via [Kadane's book site archived at archive.org](https://web.archive.org/web/20170914095926/http://uncertainty.stat.cmu.edu/)).  Lindley's book is largely nontechnical; Kadane's is mathematical, but with an emphasis on concepts, especially in the early chapters (I'd give it a &sext;, but it's more technical than other starred resources).  See also *CHANCE* magazine's interview: ["Discussing *Principles of Uncertainty* with Jay Kadane"](http://chance.amstat.org/2013/04/kadane-interview/). Lindley published an article-length overview: [&sext; "The Philosophy of Statistics"](https://www.jstor.org/stable/2681060?seq=1#page_scan_tab_contents) (2000; this was published in *The Statistician*, a Royal Statistical Society journal intended for a wide, not-too-technical audience; this journal became the magazine *Significance* in 2004, a joint publication of the RSS and the American Statistical Society).

* The **objective Bayes** viewpoint rests on the subjective Bayes foundational arguments (optimal betting), but seeks to use rule-based priors (vs. particular agents' subjective priors) as much as possible. It has a lot of overlap with the probability-as-logic viewpoint. We'll briefly look at two objective Bayes prior rules late in the course: *Jeffreys priors* (due to Harold Jeffreys), and *reference priors* (mainly due to José Bernardo and Jim Berger). Many practitioners who favor logical Bayes foundations nevertheless would happily accept "objective Bayes" as a fair description of their approach. 

## Lec03 - Key theorems

Slides:  [Lec03-KeyTheorems.pdf](Lec03-KeyTheorems.pdf)

* Bayes's theorem (BT)
* The law of total probability (LTP)
  - Extending the question/"wishful thinking"
  - Marginalization
* Normalization for exclusive, exhaustive alternatives

BT was illustrated with a binary hypothesis/binary data problem: Cancer diagnosis.

### Suggested reading/viewing

*Kruschke* Chapter 5 treats Bayes's theorem (also known as "Bayes' rule").

For fans of video lectures, Harvard statistician Joe Blitzstein covers Bayes's theorem ("conditioning") and the law of total probability in [Lecture 5: Conditioning Continued, Law of Total Probability | Statistics 110 - YouTube](https://www.youtube.com/watch?v=JzDvVgNDxo8). He discusses the Monty Hall problem in a subsequent lecture. These are chalk-on-blackboard lectures. Blitzstein is the person from whom I got the "wishful thinking" characterization of LTP that I shared in Lec04. Another colloquial characterization might be, "take everything into account."

**Case diagrams:** The "case diagrams" or "case lattices" in the binary classification/cancer diagnosis example of Lec03, are more popularly known as "natural frequency trees," a pedagogical tool that's been widely popularized by German social scientist [Gerg Gigerenzer](https://en.wikipedia.org/wiki/Gerd_Gigerenzer). (I don't use that term because the frequencies are not "natural"—they're *ideal*—and the diagram is technically not a tree.) His popular-level book, [*Calculated Risks*](http://www.simonandschuster.com/books/Calculated-Risks/Gerd-Gigerenzer/9780743254236), uses such diagrams to teach basic Bayesian reasoning. Gigerenzer has done research on teaching people how to understand risk and uncertainty; the research demonstrates the value of such tools, at least for certain audiences (medical professionals in particular).

* Cornell mathematician [Steven Strogatz](http://www.stevenstrogatz.com/), a widely-lauded popularizer of mathematics and regular NPR guest and commentator, used to write a popular math column for the *New York Times*. He covered Gigerenzer's *Calculated Risks* book in a 2010 column: [&sext; "Chances Are"  (*The New York Times*)](https://opinionator.blogs.nytimes.com/2010/04/25/chances-are/). This is a fast and fun summary of Gigerenzer's main ideas.
* For a recent presentation of some of this research, see ["Natural frequencies improve Bayesian reasoning in simple and complex inference tasks"](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4604268/) (Hoffrage et al., 2015).
* See [Gerd Gigerenzer's *Calculated Risks* site | Max Planck Institute for Human Development](https://www.mpib-berlin.mpg.de/en/research/adaptive-behavior-and-cognition/publications/books/calculated-risks) for links to more of his research.
* See [Frequency format hypothesis - Wikipedia](https://en.wikipedia.org/wiki/Frequency_format_hypothesis) for an overview of the research (with pros and cons).



## Lec04 - Inference in discrete spaces

Slides:  [Lec04-DiscreteSpaces.pdf](Lec04-DiscreteSpaces.pdf)



### Suggested reading

The last example in Lec04—the possibly biased coin problem—is a discretization of a problem that is inherently continuous (i.e., the probability for heads could be any number in $[0,1]$, which we treat in Lec05 in all its labyrinthian glory). The book, [&sext; *Think Bayes: Bayesian Statistics Made Simple*](http://greenteapress.com/wp/think-bayes/), by Allen Downey (2012), uses similar discretizations of many problems to teach Bayesian ideas in an accessible manner (including providing Python code to do the required calculations over discrete spaces). I found the book too, well, *discrete* to be a good teaching resource at the level of STSCI 4780. But Downey does a very good job covering key Bayesian concepts in the context of simple problems. The book is a free download and a quick read. It won't directly help you set up calculations for problems of realistic complexity, but it may help you better understand the fundamental ideas, which may well *indirectly* help you solve real problems. My favorite take-away from Downey's book is something simple: his introduction of the term *suite* as a convenient shorthand for "a collection of mutually exclusive, exhaustive alternatives."

## Lec05 - Continuous parameter estimation with discrete data, 1

Slides:  [Lec05-ParamEstmn-BetaBinomial.pdf](Lec05-ParamEstmn-BetaBinomial.pdf)

* The continuum: PDFs vs. PMFs
* Binary outcome data: Bernoulli, binomial, negative binomial distributions
* Beta distribution posterior PDFs
* Conjugate families (beta-Bernoulli, beta-binomial...)
* The likelihood principle

### Suggested reading

*Kruschke* Chapter 6 works through the beta-bernoulli model.

## Lec06 - Continuous parameter estimation with discrete data, 2

Slides:  [Lec06-ParamEstmn-DirichletMultinomial.pdf](Lec06-ParamEstmn-DirichletMultinomial.pdf)

* Probability and frequency:
  - Bernoulli's weak law of large numbers: predict frequency from a given probability
  - Bayes's theorem: Inferring per-trial probability from frequency data
* Categorical data: categorical and multinomial distributions
* Dirichlet distribution posterior PDFs
* Dirichlet-categorical and Dirichlet-multinomial conjugacy
* The Dirac delta function


### Suggested reading

**The Dirichlet-multinomial conjugate model:** See my [notes on this model](DirichletMultinomialNotes.pdf). This document reproduces the calculations of the lecture, but with more details. It also describes some additional calculations. I've adapted this from old notes for a colleague; as a result, some of the notation doesn't *exactly*  match the notation of Lec06 (e.g., I use $i$ rather than $k$ as the category index), but it's close. The section on model comparison won't make sense until a later lecture.

**The Dirac delta function:** The $\delta$ function is named for physicist Paul Dirac, who devised it to make some formulas in quantum mechanics easier to interpret and manipulate. He was interested in generalizing some quantum mechanics methods that were developed in discrete spaces, extending them to work in the continuum. Specifically, he aimed to generalize the *Kronecker $\delta$* symbol, $\delta_{ij}$, a common tool used in discrete sums. It's basically the identity matrix in component form:
$$
\delta_{ij} = 
  \begin{cases}
    1 & \mbox{if } i=j, \\
    0 & \mbox{if } i\ne j.
  \end{cases}
$$
In a sum with a Kronecker $\delta$ multiplying vector or matrix components, summing over a $\delta$ index eliminates the sum and causes all occurrences of that index to be replaced with the other index—i.e., it picks out a term in the sum. For example, for a vector $\vec{a}$ with components $a_j$,
$$
\sum_{j} a_{j} \delta_{ij} = a_i.
$$
Essentially, summing over $j$ picks out the $j=i$ term from the summand. The Dirac $\delta$ function works analogously: integrating $f(x)\delta(x-c)$ over $x$ replaces $x$ with $c$, returning just $f(c)$—it just sets $x=c$ everywhere in the integrand. Incidentally, the $\delta$ function is symmetric; $\delta(c-x)$ has the same effect as $\delta(x-c)$. I sometimes exploit this, choosing the order of terms in the argument of a $\delta$ function to make it more readable.

A few years after Dirac's introduction of $\delta(x)$, mathematician Laurent Schwartz put it on a firm mathematical footing, basically creating a new area of mathematics to do so: the theory of *distributions* (distinct from probability distributions) or *generalized functions* (there were hints of $\delta(x)$ and generalized functions in earlier work). The math literature in this area tends to be formal and technical, and not very accessible to non-mathematicians.

Wikipedia has a helpful article on the $\delta$ function: [Dirac delta function - Wikipedia](https://en.wikipedia.org/wiki/Dirac_delta_function). Two recent overviews by physicists are worth a look:

* [Appendix A: The Dirac Delta Function](http://onlinelibrary.wiley.com/doi/10.1002/9783527618460.app1/summary), in David Griffiths' *Introduction to Elementary Particles* (free PDF). This gives a few-page overview along the lines of the approach we took in Lec06, and includes material on transformations of $\delta$ functions that we will use later, when we cover *propagation of uncertainty* (an important application of $\delta$ functions).

* Nicholas Wheeler's "Simplified Dirac Delta" notes at [Nicholas Wheeler's Documents](http://www.reed.edu/physics/faculty/wheeler/documents/) (look under "Miscellaneous Math: Delta Functions"). This is a lengthier treatment, relating the $\delta$ function to the simpler *Heaviside step function*. Even if you're not interested in Wheeler's step function approach, the early part of his notes is very much worth reading; it provides a very accessible account of the history of the $\delta$ function. He emphasizes a point we made in class, that the $\delta$ function only really makes sense in the context of integrals, describing Schwartz's generalized functions as new mathematical entities "that live always in the shade of an implied integral sign." He quotes Dirac on this point:

  > There are a number of elementary equations which one can write down about $\delta$ functions. These equations are essentially *rules of manipulation* for algebraic work involving  $\delta$ functions. The meaning of any of these equations is that its two sides give equivalent results [when used] as *factors in an integrand*.

  Wheeler's companion article, "Delta Interrelations," explicitly demonstrates a point I made but did not demonstrate in class—that you can use a wide variety of "parameterized peak" functions to define the $\delta$ function, all of them giving the same results in the limit of an infinitesimally narrow, infinitely tall peak. We used normalized boxes; Wheeler also uses Gaussian PDFs and other functions.

## Lec07 - Continuous parameter estimation with discrete data, 3

Slides:  [Lec07-ParamEstmn-GammaPoisson.pdf](Lec07-ParamEstmn-GammaPoisson.pdf)


* The Poisson distribution
* The gamma-Poisson conjugate family


### Suggested reading

The typical derivation of the Poisson distribution in introductory statistics courses treats it as an approximation of the binomial distribution in a particular, nontrivial limit. We may cover this in a later lecture or lab. It is a simpler derivation than the first-principles approach we took in Lec07. But it masks the connection between the Poisson distribution and the Poisson point process, which I feel provides a better motivation. Our derivation, though more challenging, obtains the distribution directly as a model for the "random" distribution of events across an interval (of time or space). It illustrates some model-building ideas, makes explicit the key assumptions underlying the Poisson distribution, and provides a first exposure to a mathematical technique we'll encounter again later: solving  *functional equations* [(Wikipedia article)](https://en.wikipedia.org/wiki/Functional_equation).

If you'd like to read article/textbook derivations of the Poisson distribution along these lines, consider these sources:

* Ed Jaynes offers a different but related first-principles derivation in his article, ["Probability theory as logic"](http://bayes.wustl.edu/etj/articles/prob.as.logic.pdf) (1990). I've taught this derivation before. It treats events arriving in time, and the resulting natural ordering of the events plays an important role in the derivation. The Poisson distribution applies more generally (e.g., to unordered points in space, like the locations of trees), so I've moved away from this derivation. (Incidentally, this article appears in a conference proceedings where my first article on Bayesian methods appeared—a long review article, strongly influenced by Jaynes's prior work. I first met Jaynes at the meeting covered by this proceedings volume; it was a thrill! We became friends, and I was priveleged to speak at the memorial meeting organized on the occassion of his death in 1998.)
* One of the classic "bibles" of results in probability theory is the 2-volume opus, *An Introduction to Probability Theory and its Applications*, by William Feller. It's so admired and so widely cited that it's become known simply as *Feller*, as in: "Oh, you'll find that in *Feller*." The derivation we went through is based on Feller's derivation in section XVII.2 of Volume 1, with material on the functional equation adapted from his treatment of related birth-death processes in section XVII.6. In somewhat characteristic fashion, Feller omits details on how to actually solve the differential and functional equations he derives, stating the solutions as if they were obvious (which they probably were, to him!). My notes on how to solve the differential equation drew from a similar derivation in *Probability and random processes: An introduction for applied scientists and engineers* (1970), by Wilbur Davenport. He, too, omits details, but at least he provides hints (in problems for the reader) that helped me solve the differential equation. Feller's Volume 1 is [available online via Archive.org](https://archive.org/details/AnIntroductionToProbabilityTheoryAndItsApplicationsVolume1) (the 1957 printing; I used the 1968 printing).
* The Lec07 slides include supplementary slides on a simple nuisance parameter problem involving the Poisson distribution, sometimes called the "on/off problem." Imagine a physicist measuring the rate of production of particles (particles per sec), or an astronomer measuring the flux of light from a star (photons per sec), but in a setting where there's an unknown *background rate*. The on/off problem arises when one observes with the source "off," to provide a (noisy!) background estimate, and then with the source "on," to provide a (noisy!) estimate of the total (source + background) rate. What does this tell you about the source rate (accounting for uncertainty in the background rate)?  The Poisson on/off problem was first treated (independently) by physicist Harrison Prosper and by me in the late 1980s. This was years before the web, when it was much harder to find others' work; Harrison and I didn't learn about our mutual discovery until we met at a physics/astronomy/statistics meeting ca. 2002 (the discoveries were not quite simultaneous; his earliest, short treatment beat my longer treatment by a few years).
  - ["Small-signal analysis in high-energy physics: A Bayesian approach"](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.37.1153) (Prosper 1988). Prosper didn't present the result in a mixture-of-gamma-distributions form, but otherwise got the math right.
  - ["The promise of Bayesian inference for astrophysics"](http://www.astro.cornell.edu/staff/loredo/bayes/promise.pdf) (Loredo 1992; this contains a more pedagogical version of a shorter treatment of the problem from 1989, and a broader discussion of the importance of marginalization; it also describes treatment of a time-domain Poisson point process problem where the actual event times are recorded).

## Lec08 - Parameter estimation with continuous data—The normal (Gaussian) sampling distribution

Slides:  [Lec08-ParamEstmn-Normal.pdf](Lec08-ParamEstmn-Normal.pdf)

* The normal (Gaussian) distribution
  - Quadratic forms, completing the square, and sufficiency
* Student's $t$ distribution
* Stigler's law of eponomy




### Suggested reading

**Student's $t$ distribution:** Wikipedia has a good entry on [Student's t-distribution](https://en.wikipedia.org/wiki/Student%27s_t-distribution). You can access Gossett's 1908 paper, ["Probable error of a mean"](https://academic.oup.com/biomet/article-abstract/6/1/1/225634?redirectedFrom=fulltext), via CULib. It provides a frequentist treatment of the problem, which coincidentally leads to confidence regions that are the same as the credible regions resulting from a Bayesian treatment.

**Stigler's law of eponomy:** Besides having a good entry on [Stigler's law of eponymy](https://en.wikipedia.org/wiki/Stigler%27s_law_of_eponymy), Wikipedia also hosts a page collecting dozens of [examples of Stigler's law](https://en.wikipedia.org/wiki/List_of_examples_of_Stigler%27s_law). Stigler's 1980 paper on the topic was published in [Transactions of the New York Academy of Sciences](http://onlinelibrary.wiley.com/doi/10.1111/j.2164-0947.1980.tb02775.x/abstract). CULib does not have online access to it, but the journal volume is available in the stacks.

There's more to Stigler's law than just pointing out misattribution. One of Stigler's points is that discovery alone is not enough; you have to *make something of the discovery*. Often a discovery is named for the person who first saw the importance of the new finding, or who first made significant use of it. This article at the fascinating [Edge.org](https://www.edge.org/) web site highlights this point: ["Stigler’s Law of Eponymy"](https://www.edge.org/response-detail/27004) by William Poundstone (2017). Edge.org chooses a provocative question each year, and asks a large panel of thought leaders to draft short responses to it. This article was a response to the 2017 question: *What scientific term or concept ought to be more widely known?*

**Sufficiency:** We've now seen several examples of *sufficient statistics*, functions of the data that completely determine how the likelihood function depends on the data. The formal definition of sufficiency is a bit more abstract: a statistic (function of the data), $S(D)$, is sufficient for a sampling distribution with parameters $\theta$ if $P(D|S(D),\theta)$ does not depend on $\theta$, so that $P(D|S(D),\theta) = P(D|S(D))$. This says that once you know the value of the statistic, specifying $\theta$ itself doesn't provide any further information about the probability for the data. The *Fisher–Neyman factorization theorem* shows that this is the same as the definition that we've been using: roughly, the sufficient statistics are the functions of the data appearing in the likelihood function. Wikipedia has a good treatment of these topics: [Sufficient statistic (Wikipedia)](https://en.wikipedia.org/wiki/Sufficient_statistic).



## Lec09 — Propagating uncertainty

Slides: [Lec09-PropagatingUncertainty.pdf](Lec09-PropagatingUncertainty.pdf)

* Parametric model inference recap — parameter estimation, model comparison, etc.
* Roles for propagating uncertaint: change of variables, nuisance parameters, prediction, model comparison
* Change of variables — univariate cases
* Simple vs. compound/composite hypotheses
* Intro to handling nuisance parameters via marginalization

A good online treatment of the "change of variables" topic we covered in Lec09 and Lec10 is in the notes for Penn State's [STAT 414 / 415](https://online.stat.psu.edu/stat414/). See [Section 5: Distributions of Functions of Random Variables | STAT 414 / 415](https://online.stat.psu.edu/stat414/node/127/). We focused on the univariate case, which they treat here: [Lesson 22: Functions of One Random Variable | STAT 414 / 415](https://online.stat.psu.edu/stat414/node/128/) (follow the links at the bottom). Their treatment does *not* cover use of $\delta$ functions (which we continue to explore in Lec10). Other lessons in Section 5 treat the multivariate case, which I only briefly mentioned (noting that material you learned in multivariate calculus about Jacobians plays a role; see Lec10, slide 3). Their treatment does *not* use Jacobians, which limits its usefulness, but it does handle important special cases.

## Lec10 — Composite hypotheses, cont'd: Marginalization, model comparison, prediction

Slides: [Lec10-ModelComparisonMargPdxn.pdf](Lec10-ModelComparisonMargPdxn.pdf)

* Propagating uncertainty with $\delta$ functions — univariate change of variables reformulation; multivariate case
* Nuisance parameters, marginalization, and parameter space volume factors
* Prediction — skipped here, but see Lab05 exercise (Laplace's rule of succession) and Lec16 

* Model comparison:
  * Odds, Bayes factor, Ockham factor
  * Example: Bernoulli/binomial data: Is $\alpha = 1/2$?
  * Signal detection with additive Gaussian noise
* Model averaging
* Key idea: Parameter space volume factors

### Suggested reading

**The Bayesian Ockham's razor:** I discuss the Gaussian example of Lec10 in my 1990 paper cited above: ["From Laplace to Supernova SN 1987A: Bayesian Inference in Astrophysics"](http://www.astro.cornell.edu/staff/loredo/bayes/L90-LaplaceToSN1987A-scan.pdf); see &sect;5.3. I learned about this important feature of Bayesian model comparison from articles by Ed Jaynes and Steve Gull cited there (and I believe Steve learned it from Ed). David MacKay generalized these presentations in Chapter 2 of his 1991 PhD thesis, [&sext; Bayesian Methods for Adaptive Models](http://www.inference.org.uk/mackay/thesis.pdf); my Lec09 slides about the Ockham factor are based on his treatment, which also appears in his influential book, [&sext; *Information Theory, Inference, and Learning Algorithms*](http://www.inference.org.uk/mackay/itila/); see Chapter 28 (note that the book, published by Cambridge University Press, is available for free online; I highly recommend the chapters on Bayesian inference and Monte Carlo methods). Astronomer Bill Jefferys and statistician Jim Berger presented a self-contained, article-length treatment of the Bayesian Ockham's razor in *American Scientist*: [&sext; "Ockham's Razor and Bayesian Analysis"](http://www.jstor.org/stable/29774559) (1992).

**Confirmation theory:** *Confirmation theory* is a school of thought in the contemporary philosophy of science that seeks to account for the notion of scientific data confirming a hypothesis. One of the most influential ideas in early 20th-century philosophy of science is Karl Popper's notion that the role of *falsification* is the key distinguishing feature of scientific reasoning. I first encountered Popper's writing on this in college; not knowing of Popper's infuence, but already having some lab experience and broader knowledge of physics and astronomy, I dismissed Popper's extreme emphasis on falsification as a poor caricature of how science works, one that could be taken seriously only by someone who was not a scientist (I still feel this way!). In fact, Popper's view was the mainstream view in the philosophy of science for much of the 20th century (paired with Kuhn's ideas about *scientific revolutions*). In important cases, scientists consider some observations or experiments to *confirm* a model or theory, rather than merely failing to falsify it. Popper tried to come up with a notion of "corroboration" to address this, but his ideas along these lines failed to gain traction. Confirmation theory arose in the 1980s to account for evidence-based confirmation, and Bayesian ideas have played a key role in confirmation theory. It remains influential and continues to be refined (and criticized). Good starting points for exploring these ideas include:

* [*Scientific Reasoning: The Bayesian Approach*](http://www.opencourtbooks.com/books_n/scientific_reasoning3.htm) (1989; 3rd edn 2005), by philosophers Colin Howson and Peter Urbach. The authors published a 4pp overview of their main ideas in the journal *Nature* in 1991; see: ["Bayesian reasoning in science"](https://www.nature.com/articles/350371a0) (requires access via CULib; )
* [*Bayes or Bust? A Critical Examination of Bayesian Confirmation Theory*](https://mitpress.mit.edu/books/bayes-or-bust) (1992) by philosopher [John Earman](10.1038/350371a0).
* The online [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/index.html) (a curated collection of review articles written by philosophers) includes an article, [Confirmation (Stanford Encyclopedia of Philosophy)](https://plato.stanford.edu/entries/confirmation/), addressing the notion of confirmation more generally, but including discussion of Bayesian confirmation theory.

**$p$-values and frequentist hypothesis testing:** One of the most-used tools in frequentist statistics is the $p$-value, a quantification of how surprising an observed dataset is under a (simple) null hypothesis. Fisher introduced $p$-values as a non-frequentist (but frequentist-inspired) alternative to frequentist Neyman-Pearson hypothesis testing. Fisher and Neyman vehemently disagreed on the soundness of using $p$-values; Jeffreys (their contemporary) also criticized $p$-values. Nevertheless, $p$-value testing is easier to do than N-P testing, and the $p$-value seems to account for evidence that is omitted in N-P Type I and Type II error rates, so $p$-values soon came to dominate practice in statistical hypothesis testing. However, criticism of $p$-values continued through the 20th century, and has become particularly intense in the 21st century. I've put together some slides on $p$-values for summer schools on statistics for astronomers; see these slides for a quick overview of some of the issues with $p$-values, the relationship between $p$-values and Bayes factors, and entry points to the literature:

* ["Just call it a '$p$-value'—not a hypothesis probability, not a false alarm probability"](cast16-PValueNote.pdf)


Of the many references cited there, my favorite is Jim Berger's ASA Fisher award lecture (I was at the ASA meeting where Jim got the award and presented this lecture; it was one of the best scientific talks I've ever heard):

* [&sext; "Could Fisher, Jeffreys and Neyman Have Agreed on Testing?" by James Berger (2003)](https://projecteuclid.org/euclid.ss/1056397485)




## Lec11 — Intro to Bayesian computation

Slides: [Lec11-BayesianComputationIntro.pdf](Lec11-BayesianComputationIntro.pdf)



* Parameter space volume; roles of the prior
* Bayesian computation setup for parameter estimation problems
* Asymptotic approximation and the Laplace approximation
* Quadrature and cubature for modest-dimensional Bayesian computation




## Lec12 — IID Monte Carlo integration

Slides: [Lec12-BayesCompn-IIDMonteCarlo.pdf](Lec12-BayesCompn-IIDMonteCarlo.pdf)



* Posterior sampling
* Expectations and sample averages
  * Sample mean is unbiased for **ID** (identically distributed) samples
  * Standard deviation is $\sigma/\sqrt{N}$ for **IID** samples
* (Weak) law of large numbers (LLN) bounds the probability of making an error of given magnitude, for any sample size
* Central limit theorem gives the asymptotic (sample size $\righarrow\infty$) PDF of the error
* Two IID sample generation methods:
  * Inverse CDF method
  * Accept/reject method


### Suggested reading

The late Sir David MacKay's 1998 "Introduction to Monte Carlo methods" is a self-contained introduction to IID Monte Carlo and Markov Chain Monte Carlo (MCMC). A revised treatment (slightly improved and visually more readable) comprises Chapter 29 of David's 2003 book.  Both are free downloads from his website:

* "Introduction to Monte Carlo methods," via [David MacKay: Publications: Monte Carlo methods](http://www.inference.org.uk/mackay/BayesMC.html)
* Chapter 29 of [&sext; *Information Theory, Inference, and Learning Algorithms*](http://www.inference.org.uk/mackay/Book.html)

For a treatment between article-length and book-length, by statisticians but staying accessible, see these lecture notes:

* [&sext; *Monte Carlo Methods: Lecture Notes* by Adam Johansen and Ludger Evers (2007)](https://warwick.ac.uk/fac/sci/statistics/staff/academic-research/johansen/teaching/mcm-2007.pdf)

For a book-length treatment of these topics from a statistician's perspective, a popular, comprehensive, but somewhat technical reference is:

* [*Monte Carlo Statistical Methods* by Christian Robert and George Casella (2004) | SpringerLink](https://link.springer.com/book/10.1007/978-1-4757-4145-2) (a free download via CULib)

The same authors have a more practical treatment, with examples in R, in:

* [*Introducing Monte Carlo Methods with R* by Christian Robert and George Casella (2010) | SpringerLink](https://link.springer.com/book/10.1007/978-1-4419-1576-4) (a free download via CULib)

For a good article-length treatment of IID Monte Carlo from a physicist's perspective (emphasizing concepts over technical results), see:

* ["Monte Carlo theory and practice" by Fred James (1980)](http://iopscience.iop.org/article/10.1088/0034-4885/43/9/002)




## Lec13 — Markov chain Monte Carlo, 1

Slides: [Lec13-MarkovChainMonteCarlo-1.pdf](Lec13-MarkovChainMonteCarlo-1.pdf)



* Euler and averaging (historical aside!)
* Markov chains, stationary Markov chains
* Matrix representation of 2-state Markov chains; eigenfunctions
* Equilibrium distributions and detailed balance/reversibility


### Suggested reading

*Monte Carlo Methods: Lecture Notes*, cited above, devotes a section to Markov chains.

My discussion of equilibrium distributions and the detailed balance condition is heavily influenced by two articles (the 2nd is probably most relevant to STSCI 4780 students):

* ["Introduction to algorithms for Monte Carlo simulations and their application to QCD" by D. Toussaint (1989)](https://www.sciencedirect.com/science/article/pii/0010465589900544)
* [&sext; "Understanding the Metropolis-Hastings Algorithm" by Siddhartha Chib and Edward Greenberg (1995)](https://www.jstor.org/stable/2684568)

The latter article is from [*The American Statistician*](https://www.tandfonline.com/toc/utas20/current), an ASA journal that publishes general-interest articles on statistics and the teaching of statistics. It's a good source of sound statistical information for non-statistician readers. The journal [*Statistical Science*](http://www.imstat.org/sts/) plays a similar role, but at a higher (but still accessible) technical level; it's published by the Institute of Mathematical Statistics (IMS).

## Lec14 — Markov chain Monte Carlo, 2

Slides: [Lec14-MarkovChainMonteCarlo-2.pdf](Lec14-MarkovChainMonteCarlo-2.pdf)



* The Metropolis-Hastings algorithm—reversible transitions via proposal distributions
* Proposal distributions
  * Acceptance/mixing rate tradeoff
  * Random walk Metropolis (RWM)
  * Independent Metropolis
* Tangent: Importance sampling
* Historical tangent: Euler on averaging



### Suggested reading

Many of the references cited above for lectures 12 and 13 cover the Metropolis-Hastings algorithm and RWM (independent Metropolis is useful to know about, but seldom used due to the difficulty of devising a proposal distribution resembling the full posterior PDF). The material by MacKay, the Johansen & Evers lecture notes, and the Chib and Greenberg article are probably the best sources of material at the level of lecture 14.

For a first-person account of the origin of these methods, see physicist Nicholas Metropolis's article, ["The Beginning of the Monte Carlo Method" (1987)](http://library.lanl.gov/cgi-bin/getfile?15-12.pdf), in the [special issue of *Los Alamos Science*](http://la-science.lanl.gov/lascience15.shtml) devoted to Stanislaw Ulam, a mathematician colleague of Metropolis who collaborated with Metropolis on Monte Carlo methods.  The `Stan` probabilistic programming language is named for Ulam.

The Metropolis-Hastings algorithm is a generalization of the simpler MCMC algorithm introduced by Metropolis *et al*. (1953); it was presented by Hastings in 1970:

* ["Monte Carlo sampling methods using Markov chains and their applications" by W. K. Hastings (1970)](https://academic.oup.com/biomet/article/57/1/97/284580)

There is a huge literature on MCMC, covering the introductory material of lecture 14 and building on it in dozens of different ways. The Robert & Casella books cited above are popular book-length treatments for statisticians. Nearly every modern book on Bayesian statistics/data analysis treats MCMC at some level, including the three books recommended for the course (*Kruschke*, *Rethinking*, and *BDA3*). Some noteworthy additional references are the following:

* [&sext; *Handbook of Markov Chain Monte Carlo*, ed. by Brooks et al. (2011)](http://www.mcmchandbook.net/) — A collection of review articles covering much of MCMC practice as of 2011. A few chapters are available online; these two are strongly recommended (the first is a must-read):
  - [&sext; "Introduction to MCMC"](http://www.mcmchandbook.net/HandbookChapter1.pdf) by [Charles Geyer](http://www.stat.umn.edu/~charlie/)
  - [&sext; "Inference and Monitoring Convergence"](http://www.mcmchandbook.net/HandbookChapter6.pdf) by Gelman and Shirley
* ["An Introduction to MCMC for Machine Learning" by Andrieu et al. (2003)](https://link.springer.com/article/10.1023/A:1020281327116) — This is a widely-cited review article aimed at computer scientists and applied researchers. It's a very good article-length treatment.
* [*Monte Carlo Strategies in Scientific Computing* by Jun Liu (2004)](https://link.springer.com/book/10.1007/978-0-387-76371-2#about) — One of the earliest book-length surveys of advanced MCMC methods. It's widely cited, but perhaps more because of the paucity of alternatives than because of its quality (colleagues have warned me that there are numerous typos/errors). (free download via CULib)
* [*Monte Carlo Methods in Bayesian Computation* by Chen et al. (2000)](https://link.springer.com/book/10.1007/978-1-4612-1276-8#toc) — The comments on Liu's book apply here, too (though not in regard to typos/errors). (free download via CULib)

