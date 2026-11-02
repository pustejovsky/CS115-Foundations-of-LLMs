# CS 115 / COSI 115B — Foundations of Large Language Models

Course materials for **261COSI-115B-1: Fundamentals of Natural Language Processing II**,
Brandeis University, Spring 2026 — taught by [James Pustejovsky](https://www.cs.brandeis.edu/~jamesp/),
with Teaching Assistant Tim.

This repository is a preserved export of the course Moodle site
(`moodle.brandeis.edu/course/view.php?id=4421`, exported 2 November 2026). The original
directory layout is kept **exactly as Moodle produced it**, so the whole site can be
browsed offline: open [`index.html`](index.html) in a browser and every lecture, quiz,
homework and reading links through as it did on Moodle.

---

## Browsing the course

| Entry point | What it is |
| --- | --- |
| [`index.html`](index.html) | The course front page — the full topic outline with links to every item |
| [`about.html`](about.html) | Course summary page |
| [`moodle-export.html`](moodle-export.html) | Moodle's own front page, kept verbatim |
| `shared/moodle.css` | Moodle's stylesheet, needed for the pages to render properly |
| `overviewfiles/` | The course banner image |

Each course item lives in its own directory named
`<Type>_<Title>_.<Moodle id>`, for example
`File_Self-Attention_and_Trans..._.392424`. Inside each one:

```
File_Self-Attention_and_Trans..._.392424/
├── index.html      # the Moodle page for this item (title, description, link)
└── content/
    └── NLP_II__Tranformers_.pdf   # the actual slides / handout / reading
```

Forum, Assignment and URL items contain only `index.html`
(their submissions and posts are not part of a content export).

The site header has a **Search** button (`⌘K`/`Ctrl K`) that searches titles,
subtitles and the full text of every mirrored PDF/HTML reading, built from
[`search-index.json`](search-index.json). After adding, removing or renaming a
reading in `index.html`, regenerate it with:

```bash
python3 tools/build_search_index.py
```

(requires `pdftotext`, from `poppler` — `brew install poppler`).

---

## Course outline

### Part I — Linguistics, Syntax, and Learning to Classify

Where NLP meets the age of big data and LLMs, a review of syntax and parsing, and the
perceptron and logistic regression as the first learning algorithms.

- Course Intro Slides · `cs115b_intro_slides.pdf`
- Linguistics in the Age of Big Data and LLMs · `linguistics_in_age_of_data.pdf`
- Evaluation Methods in NLP · `evaluation-lecture.pdf`
- Elements of Syntax for Parsing · `syntax-lecture.pdf`
- CKY Algorithm, Chomsky Normal Form · `cky-slides-2026.pdf`
- Pop quiz questions from 1/20/26 (CFGs) · `PopupQuestions-CFG.pdf`
- PCFGs · `NLP_II__PCFG_.pdf`
- Pop-up Quiz and Answers (CFGs) · `PopupQuestions-CFG.pdf`
- Perceptron Learning · `perceptron-lecture-v2.pdf`
- Linear Separability · `linear-separability.pdf`
- Linear Regression — Where Learning Begins · `linear-regression-lecture.pdf`
- Logistic Regression and the Perceptron: The Math · `NLP_II__Logistic_Regression_and_Perceptron_.pdf`

### Part II — Distributional Semantics and Neural Networks

Count-based vector spaces through SVD and prediction-based embeddings, neural network
fundamentals, structured prediction, and neural dependency parsing.

- Distributional Semantics — SVDs, Word2Vec · `distributional-semantics-lecture.pdf`
- Hierarchical Softmax for Word2Vec · `word2vec-trees.pdf`
- Latent Semantic Analysis · `lsa_lsi_slides.pdf`
- PMI, PPMI, and SVD · `pmi_ppmi_svd.pdf`
- Fundamentals of Neural Network Architectures · `Neural_Networks_NLMs.pdf`
- Distributional Semantics and Neural Networks · `NLP_II__Distributional_Semantics_and_NN_.pdf`
- Computation Graphs and Back Propagation · `computation_graphs.pdf`
- Pop-up Quiz and Answers (distributional semantics) · `distrib_sem_quiz_answers.pdf`
- Structured Prediction · `structured_prediction.pdf`
- Examples of Structured Prediction — Tagging and NER · `Detailed Examples for Structured Prediction - Tagging and NER.pdf`
- Neural Dependency Parsing · `neural_dependency_parsing.pdf`

### Part III — Sequence Models: CNNs and RNNs

Convolutional and recurrent networks for NLP, the last stop before attention.

- Introduction to CNNs · `cnn1.pdf`
- CNNs — slides from March 10, 2026 · `cnns_for_nlp.pdf`
- RNNs — slides from March 13, 2026 · `rnns_for_nlp.pdf`
- Pop Quiz Questions and Answers for CNNs and RNNs · `Popquiz-CCN-RNN.pdf`

### Part IV — Attention, Transformers, and Large Language Models

Attention and its scoring, the transformer decoder, subtoken and positional encodings,
scaling, post-training, reinforcement learning, and mixture-of-experts models.

- Attention in NLP · `rnns_for_nlp.pdf`
  *(this item links to the same slide deck as "RNNs — slides from March 13, 2026" in the
  original Moodle export; kept as-is for fidelity)*
- Methods of Scoring Attention in NMT · `attention_scoring_deck.pdf`
- Backprop Math, Optimizers, Dependency Parsing, Attention · `NLP_II__Math___LLMs_.pdf`
- A Step-by-step Analysis of a Decoder Model · `lecture_inside_transformer.pdf`
- Subtoken Encoding Strategies for LLMs · `subtoken-encoding.pdf`
- Positional Encoding Embeddings · `positional_encoding_lecture-final.pdf`
- Calculating Parameter Sizes in LLMs · `LLM-ParameterCount-Beamer.pdf`
- Self-Attention and Transformers · `NLP_II__Tranformers_.pdf`
- Introduction to Reinforcement Learning · `rl_intro_nlp2.pdf`
- Post-training for LLMs · `post_training_llms_beamer.pdf`
- Scaling (condensed slides) · `scaling_laws_condensed.pdf`
- Scaling (full lecture) · `scaling_laws_lecture.pdf`
- Mixture of Experts Models · `moe_agentic_v2.pdf`

### Assessments

- Quiz 1 Review · `NLP_II__Quiz_1_Review_.pdf`, plus Quiz 1 (Assignment — submissions not included)
- Quiz 2 Review · `NLP_II_Quiz_2_Review.pdf`, Quiz 2 Kahoot (external quiz tool), plus Quiz 2 (Assignment — submissions not included)
- Homework 1–4 (Assignments — submissions not included)
- NLP Tutorials · `NLP_II__Tutorial_Day_.pdf`
- Final Project Proposal, Final Project, Final Project Presentations (Assignments — submissions not included)

### Course information

- Full Lecture Schedule, Meeting Times, Office Hours, Grade Breakdown (Text and media areas)
- (E) Natural Language Processing — Eisenstein, and (JM) Speech and Language Processing —
  Jurafsky & Martin (external links — see below)
- News & Announcements, Ask the Class (Forums)

---

## Readings not included

Both textbooks referenced in the course are **external links in the original Moodle
site itself** — Moodle never mirrored a copy of either, so there is nothing to exclude
here. Each links out to a free copy from its authors:

| Reading | Where to get it |
| --- | --- |
| Jurafsky & Martin, *Speech and Language Processing*, 3rd ed. draft | Free from the authors: [web.stanford.edu/~jurafsky/slp3](https://web.stanford.edu/~jurafsky/slp3/) |
| Eisenstein, *Natural Language Processing* (course notes) | Free from the author: [github.com/jacobeisenstein/gt-nlp-class](https://github.com/jacobeisenstein/gt-nlp-class) |

Every PDF actually included in this repository is James Pustejovsky's own lecture
material (slides, handouts, quiz reviews) — no third-party copyrighted readings are
mirrored here, so unlike the companion CS135 site, nothing needed to be gitignored.

---

## Licensing

The lecture slides, handouts and quiz reviews are course materials by James Pustejovsky,
shared here for students and for reference. They are not placed in the public domain —
please credit the author and the course if you reuse them. The two linked textbooks above
remain under their own authors' terms.
