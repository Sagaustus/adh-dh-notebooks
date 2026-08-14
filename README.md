# Computational Text Analysis for African Digital Humanities

**112 runnable notebooks**, organised by method. Every one executes top to bottom — enforced by the build, not assumed.

Companion to the course at [coursehub.africandigitalhumanities.ca](https://coursehub.africandigitalhumanities.ca/courses/computational-text-analysis-african-dh/), where the same notebooks run in the browser with no setup.

## The data loads itself

Open any notebook in Colab and run the first cell. It downloads what it needs from `coursehub.africandigitalhumanities.ca/ide/pack-data/text/` — **no uploading, no API key, no account.**

| Corpus | What it is | Licence |
|---|---|---|
| `masakhanews.csv` | News in 16 African languages with topic labels | AFL-3.0 |
| `masakhaner.csv` | MasakhaNER 2.0 — 147,053 sentences, 19 languages, official splits | CC BY 4.0 |
| `colonial_texts.csv` | Passages from pre-1929 writing about Africa | Public domain |
| `african_legal.csv` | ECOWAS, ANC and TRC documents | Public / open |
| `labse_headlines.npy` | Precomputed LaBSE vectors, so neural lessons work with no GPU | derived |

## Where the GPU comes from

- **In Colab** — your own free GPU (`Runtime > Change runtime type > T4`).
- **In CourseHub** — a shared L40S, via an endpoint whose credential stays on the server.
- **Anywhere else** — precomputed vectors shipped with the course.

No API key appears anywhere in this repository, by design: a notebook cell is readable by whoever runs it.

## Contents

### 00-foundations

Where the field came from, and how to turn a humanities question into a countable one.

| Notebook | Method | Open |
|---|---|---|
| [Text as Data](00-foundations/00_text_as_data.ipynb) | Turning a corpus into a table: document, token, type | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/00_text_as_data.ipynb) |
| [Practice: Your First Hour With an Unfamiliar Corpus](00-foundations/00b_practice_first_look.ipynb) | A reproducible first-look protocol before any analysis | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/00b_practice_first_look.ipynb) |
| [What a Corpus Can and Cannot Answer](00-foundations/01a_what_a_corpus_answers.ipynb) | Matching a literary or linguistic question to a countable method | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/01a_what_a_corpus_answers.ipynb) |
| [Whose Africa Is in the Public Domain?](00-foundations/01b_whose_africa_is_public_domain.ipynb) | Corpus construction as an argument; the absence audit for text | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/01b_whose_africa_is_public_domain.ipynb) |
| [Practice: Match Your Question to a Method](00-foundations/01c_practice_match_question.ipynb) | Turning a humanities question into a countable one, or deciding it is not | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/01c_practice_match_question.ipynb) |
| [Busa, the Concordance, and Where All This Came From](00-foundations/21a_busa_and_the_concordance.ipynb) | Index verborum and KWIC as the founding method; reconstructing the workflow | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/21a_busa_and_the_concordance.ipynb) |
| [Practice: Build the Instrument Busa Built](00-foundations/21b_practice_build_a_concordance.ipynb) | A complete index verborum and concordance, then a reading from it | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/00-foundations/21b_practice_build_a_concordance.ipynb) |

### 01-preparing-text

Tokenising, normalising, stemming, morphology and OCR error — the decisions every later number inherits.

| Notebook | Method | Open |
|---|---|---|
| [Stopwords Are Not Universal](01-preparing-text/03a_stopwords_are_not_universal.ipynb) | Stopword removal; why English lists do nothing to African languages | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/03a_stopwords_are_not_universal.ipynb) |
| [Diacritics and the ASCII Trap](01-preparing-text/03b_diacritics_and_the_ascii_trap.ipynb) | Unicode-aware tokenising; measuring what naive cleaning destroys | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/03b_diacritics_and_the_ascii_trap.ipynb) |
| [Practice: How Much Does Preprocessing Change Your Result?](01-preparing-text/03c_practice_preprocessing.ipynb) | One finding, five preprocessing pipelines, and the spread between them | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/03c_practice_preprocessing.ipynb) |
| [Stemming, Lemmatisation, and Why Preprocessing Is Not Neutral](01-preparing-text/14a_stemming_and_lemmatisation.ipynb) | Suffix stripping vs dictionary lookup; Schofield & Mimno's warning | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/14a_stemming_and_lemmatisation.ipynb) |
| [Finite-State Morphology: Rules That Run Both Ways](01-preparing-text/14b_finite_state_morphology.ipynb) | Two-level morphology; a reversible analyser/generator for Swahili verbs | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/14b_finite_state_morphology.ipynb) |
| [Historical Spelling and Orthographic Normalisation](01-preparing-text/14c_historical_normalisation.ipynb) | Edit distance, phonetic matching and rewrite rules; the VARD/Norma approach | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/14c_historical_normalisation.ipynb) |
| [OCR Error and How It Propagates](01-preparing-text/14d_ocr_error_propagation.ipynb) | Character error rate; measuring the downstream cost of noisy text | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/14d_ocr_error_propagation.ipynb) |
| [Practice: Audit a Preparation Pipeline End to End](01-preparing-text/14e_practice_pipeline_audit.ipynb) | Tracing one document through every preparation step and costing each | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/01-preparing-text/14e_practice_pipeline_audit.ipynb) |

### 02-describing-corpora

Frequency, Zipf, vocabulary richness, document length.

| Notebook | Method | Open |
|---|---|---|
| [Word Frequency](02-describing-corpora/02a_word_frequency.ipynb) | Frequency distributions; raw counts vs normalised rates | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02a_word_frequency.ipynb) |
| [Zipf's Law](02-describing-corpora/02b_zipfs_law.ipynb) | Rank-frequency distributions; the long tail and what it costs you | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02b_zipfs_law.ipynb) |
| [Type/Token Ratio and Its Trap](02-describing-corpora/02c_type_token_ratio.ipynb) | Vocabulary richness; length dependence and standardised TTR | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02c_type_token_ratio.ipynb) |
| [Document Length as Evidence](02-describing-corpora/02d_document_length.ipynb) | Distributions of length; median vs mean; when a skew is the finding | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02d_document_length.ipynb) |
| [Vocabulary Richness Beyond TTR](02-describing-corpora/02e_vocabulary_richness.ipynb) | Yule's K, Herdan's C, MATTR and Heaps's law; length-robust richness | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02e_vocabulary_richness.ipynb) |
| [Practice: Does Nigerian-Language News Look Different?](02-describing-corpora/02f_practice_describing.ipynb) | A description worked end to end: length, richness, and what they license | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/02-describing-corpora/02f_practice_describing.ipynb) |

### 03-comparing-corpora

Keyness, effect size, concordance and collocation.

| Notebook | Method | Open |
|---|---|---|
| [Keyness: Which Words Distinguish a Corpus](03-comparing-corpora/04a_keyness.ipynb) | Log-likelihood keyness; target vs reference corpus | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/04a_keyness.ipynb) |
| [Effect Size for Words](03-comparing-corpora/04b_effect_size_for_words.ipynb) | Why significance is not importance; log ratio and %DIFF | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/04b_effect_size_for_words.ipynb) |
| [Comparing Across Archives](03-comparing-corpora/04c_comparing_across_archives.ipynb) | Keyness between unlike corpora; confounds you cannot remove | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/04c_comparing_across_archives.ipynb) |
| [Why Significance Stops Meaning Anything](03-comparing-corpora/04d_significance_and_its_critics.ipynb) | The Kilgarriff/Gries/Koplenig debate, demonstrated by resampling | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/04d_significance_and_its_critics.ipynb) |
| [Practice: What Distinguishes Health Coverage, Robustly?](03-comparing-corpora/04e_practice_comparing.ipynb) | Keyness with effect size, dispersion and a robustness check, end to end | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/04e_practice_comparing.ipynb) |
| [KWIC: Reading What a Count Points At](03-comparing-corpora/05a_kwic_concordance.ipynb) | Keyword-in-context; using a count to direct close reading | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/05a_kwic_concordance.ipynb) |
| [Collocation: The Company a Word Keeps](03-comparing-corpora/05b_collocation.ipynb) | Window co-occurrence; span and its effect on results | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/05b_collocation.ipynb) |
| [Association Measures: PMI, Dice and Log-Likelihood](03-comparing-corpora/05c_association_measures.ipynb) | Choosing an association statistic and knowing what it favours | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/05c_association_measures.ipynb) |
| [t-score, log-Dice and Delta P](03-comparing-corpora/05d_association_measures_completed.ipynb) | The association measures the field actually reports, and their biases | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/05d_association_measures_completed.ipynb) |
| [Practice: What Company Does 'Government' Keep?](03-comparing-corpora/05e_practice_collocation.ipynb) | Collocation to concordance and back; a reading grounded in counts | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/03-comparing-corpora/05e_practice_collocation.ipynb) |

### 04-rule-based-methods

Regex as method, a corpus query language, gazetteers, dictionary content analysis.

| Notebook | Method | Open |
|---|---|---|
| [Regular Expressions as Scholarly Method](04-rule-based-methods/15a_regex_as_method.ipynb) | Pattern extraction as evidence; precision, recall and the Unicode trap | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/04-rule-based-methods/15a_regex_as_method.ipynb) |
| [A Corpus Query Language of Your Own](04-rule-based-methods/15b_corpus_query_language.ipynb) | CQL/CQP semantics; querying token sequences rather than characters | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/04-rule-based-methods/15b_corpus_query_language.ipynb) |
| [Gazetteers and Rule-Based Extraction](04-rule-based-methods/15c_gazetteers_and_rules.ipynb) | ANNIE/JAPE-style entity extraction; when rules beat statistical NER | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/04-rule-based-methods/15c_gazetteers_and_rules.ipynb) |
| [Dictionary-Based Content Analysis and Its Limits](04-rule-based-methods/15d_dictionary_content_analysis.ipynb) | General Inquirer-style category counting; why sentiment lexicons fail here | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/04-rule-based-methods/15d_dictionary_content_analysis.ipynb) |
| [Practice: Extract an Entity Type With No Training Data](04-rule-based-methods/15e_practice_rules_vs_stats.ipynb) | Building, measuring and iterating a rule set against a hand-checked sample | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/04-rule-based-methods/15e_practice_rules_vs_stats.ipynb) |

### 05-unsupervised-structure

TF-IDF, clustering, LSA and topic models.

| Notebook | Method | Open |
|---|---|---|
| [Vectorising Text: TF-IDF](05-unsupervised-structure/06a_vectorising_text.ipynb) | Document–term matrices; term weighting and what min_df does | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/06a_vectorising_text.ipynb) |
| [Clustering Documents with K-Means](05-unsupervised-structure/06b_clustering_documents.ipynb) | K-means on TF-IDF; choosing k and reading clusters honestly | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/06b_clustering_documents.ipynb) |
| [Dendrograms: Clustering Without Choosing K](05-unsupervised-structure/06c_dendrograms.ipynb) | Hierarchical clustering; linkage choice and cutting the tree | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/06c_dendrograms.ipynb) |
| [LSA and LSI: Where Document Vectors Came From](05-unsupervised-structure/06d_lsa_and_the_vector_lineage.ipynb) | Truncated SVD on a term-document matrix; the ancestor of embeddings | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/06d_lsa_and_the_vector_lineage.ipynb) |
| [Practice: Does This Corpus Cluster by Topic or by Language?](05-unsupervised-structure/06e_practice_clustering.ipynb) | Unsupervised structure, and testing what the clusters actually track | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/06e_practice_clustering.ipynb) |
| [Topic Modelling with LDA](05-unsupervised-structure/08a_topic_modelling_lda.ipynb) | Latent Dirichlet Allocation; documents as mixtures of topics | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/08a_topic_modelling_lda.ipynb) |
| [NMF: The Other Topic Model](05-unsupervised-structure/08b_nmf_topics.ipynb) | Non-negative matrix factorisation; comparing two models on one corpus | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/08b_nmf_topics.ipynb) |
| [Reading Topics Sceptically](05-unsupervised-structure/08c_reading_topics_sceptically.ipynb) | Choosing k; coherence; the topics that are artefacts | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/08c_reading_topics_sceptically.ipynb) |
| [Are Topics Evidence? Coherence and Its Critics](05-unsupervised-structure/08d_are_topics_evidence.ipynb) | NPMI coherence; Chang's 'reading tea leaves'; Schmidt's 'Words Alone' | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/08d_are_topics_evidence.ipynb) |
| [Practice: Are These Topics Worth Reporting?](05-unsupervised-structure/08e_practice_topics.ipynb) | A topic model from k-selection to a defensible written interpretation | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/05-unsupervised-structure/08e_practice_topics.ipynb) |

### 06-supervised-classification

Classifiers, sequence labelling, and the annotation work that makes labels trustworthy.

| Notebook | Method | Open |
|---|---|---|
| [Train and Test: The Split That Makes a Number Mean Something](06-supervised-classification/07a_train_test_on_text.ipynb) | Held-out evaluation; leakage; the majority-class baseline | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/07a_train_test_on_text.ipynb) |
| [Features and Models: What Actually Moves the Number](06-supervised-classification/07b_features_and_models.ipynb) | Comparing feature settings and classifiers; cross-validation | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/07b_features_and_models.ipynb) |
| [Which Words Carry the Decision](06-supervised-classification/07c_which_words_carry_the_decision.ipynb) | Model coefficients as evidence; interpreting a linear classifier | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/07c_which_words_carry_the_decision.ipynb) |
| [Practice: Build a Classifier You Could Defend](06-supervised-classification/07d_practice_classifier.ipynb) | A supervised study end to end: baseline, model, errors, and honest reporting | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/07d_practice_classifier.ipynb) |
| [Tagging a Sequence: Hidden Markov Models and Viterbi](06-supervised-classification/16a_hmm_pos_tagging.ipynb) | HMM tagging from scratch; emission and transition probabilities; Viterbi | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/16a_hmm_pos_tagging.ipynb) |
| [Features, Not Just Words: Toward CRFs](06-supervised-classification/16b_features_and_crfs.ipynb) | Feature engineering for sequence models; why CRFs replaced HMMs | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/16b_features_and_crfs.ipynb) |
| [Practice: Is an Off-the-Shelf Tagger Good Enough for Your Corpus?](06-supervised-classification/16c_practice_tagging_project.ipynb) | Evaluating a tagger on your own material before depending on it | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/16c_practice_tagging_project.ipynb) |
| [Coding a Corpus, and Cohen's Kappa](06-supervised-classification/17a_coding_and_cohens_kappa.ipynb) | Coding schemes; raw agreement vs chance-corrected agreement | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/17a_coding_and_cohens_kappa.ipynb) |
| [Krippendorff's Alpha: Agreement That Generalises](06-supervised-classification/17b_krippendorffs_alpha.ipynb) | Alpha for any number of coders, missing data and measurement levels | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/17b_krippendorffs_alpha.ipynb) |
| [Practice: Build a Coding Scheme and Test It](06-supervised-classification/17c_practice_coding_scheme.ipynb) | From category definitions to a measured agreement figure | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/06-supervised-classification/17c_practice_coding_scheme.ipynb) |

### 07-stylometry

Authorship attribution from Mosteller and Wallace to Cosine Delta and Zeta.

| Notebook | Method | Open |
|---|---|---|
| [Most-Frequent Words: The Signal Everyone Discards](07-stylometry/09a_most_frequent_words.ipynb) | MFW feature sets; why function words identify authors | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09a_most_frequent_words.ipynb) |
| [Burrows's Delta](07-stylometry/09b_burrows_delta.ipynb) | Z-scored MFW plus a distance measure; the standard attribution method | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09b_burrows_delta.ipynb) |
| [Style Beyond Authorship](07-stylometry/09c_style_beyond_authorship.ipynb) | Stylometric features for genre, register and translation | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09c_style_beyond_authorship.ipynb) |
| [Delta Variants: Cosine, Eder, and the MFW Question](07-stylometry/09d_delta_variants.ipynb) | Comparing Delta measures and MFW bands; bootstrap consensus trees | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09d_delta_variants.ipynb) |
| [Zeta and Character N-grams](07-stylometry/09e_zeta_and_character_ngrams.ipynb) | Craig's Zeta on mid-frequency words; character n-gram attribution | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09e_zeta_and_character_ngrams.ipynb) |
| [Mosteller and Wallace: The Federalist Papers](07-stylometry/09f_mosteller_and_wallace.ipynb) | The founding authorship study; Bayesian reasoning on function words | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09f_mosteller_and_wallace.ipynb) |
| [Practice: Attribute an Anonymous Work](07-stylometry/09g_practice_attribution.ipynb) | A full attribution study, with the checks that make it publishable | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/07-stylometry/09g_practice_attribution.ipynb) |

### 08-text-reuse-and-networks

Shingling, MinHash and alignment; collocation and character networks.

| Notebook | Method | Open |
|---|---|---|
| [Shingling: Finding Reuse Without Reading](08-text-reuse-and-networks/18a_shingling_and_jaccard.ipynb) | Character and word shingles; Jaccard similarity; the quadratic wall | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/18a_shingling_and_jaccard.ipynb) |
| [MinHash and LSH: Reuse Detection That Scales](08-text-reuse-and-networks/18b_minhash_and_lsh.ipynb) | Signature sketching and locality-sensitive hashing; sub-quadratic search | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/18b_minhash_and_lsh.ipynb) |
| [Aligning Reuse, and Reading What Changed](08-text-reuse-and-networks/18c_aligning_and_reading_reuse.ipynb) | Sequence alignment on detected pairs; editing as evidence | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/18c_aligning_and_reading_reuse.ipynb) |
| [Practice: Trace a Story Across a Corpus](08-text-reuse-and-networks/18d_practice_reuse_study.ipynb) | Detection, filtering, clustering and the direction problem | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/18d_practice_reuse_study.ipynb) |
| [Collocation Networks](08-text-reuse-and-networks/19a_collocation_networks.ipynb) | Building and reading a GraphColl-style collocation network | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/19a_collocation_networks.ipynb) |
| [Character and Entity Networks](08-text-reuse-and-networks/19b_character_networks.ipynb) | Co-occurrence networks of people; Moretti's plot networks and their critics | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/19b_character_networks.ipynb) |
| [Practice: Make a Network Claim You Can Defend](08-text-reuse-and-networks/19c_practice_network_argument.ipynb) | Building a network, testing its stability, and stating what it shows | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/08-text-reuse-and-networks/19c_practice_network_argument.ipynb) |

### 09-encoding-as-method

TEI-XML, XPath and standoff annotation. Encoding is interpretation.

| Notebook | Method | Open |
|---|---|---|
| [TEI-XML: Encoding Is Interpretation](09-encoding-as-method/20a_tei_and_what_markup_asserts.ipynb) | TEI P5 structure; markup as a scholarly claim rather than formatting | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/09-encoding-as-method/20a_tei_and_what_markup_asserts.ipynb) |
| [Querying TEI with XPath](09-encoding-as-method/20b_querying_tei_with_xpath.ipynb) | XPath over encoded text; structural queries a plain-text search cannot make | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/09-encoding-as-method/20b_querying_tei_with_xpath.ipynb) |
| [Standoff Annotation and CoNLL-U](09-encoding-as-method/20c_standoff_and_conllu.ipynb) | Character-offset annotation; overlapping hierarchies; interchange formats | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/09-encoding-as-method/20c_standoff_and_conllu.ipynb) |
| [Practice: Encode One Page, and Argue With Yourself](09-encoding-as-method/20d_practice_encode_a_page.ipynb) | A full TEI encoding decision log, and querying what you asserted | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/09-encoding-as-method/20d_practice_encode_a_page.ipynb) |

### 10-visualising-and-arguing

Charts that carry an argument, dispersion, and turning counts into prose.

| Notebook | Method | Open |
|---|---|---|
| [Charting Frequency and Difference](10-visualising-and-arguing/10a_charting_frequency.ipynb) | Bar charts, ranked comparisons, and the axis decisions that mislead | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/10a_charting_frequency.ipynb) |
| [Why Word Clouds Mislead](10-visualising-and-arguing/10b_why_word_clouds_mislead.ipynb) | Diagnosing a visualisation; area perception and the alternatives | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/10b_why_word_clouds_mislead.ipynb) |
| [Dispersion: Where in a Text a Word Appears](10-visualising-and-arguing/10c_dispersion_and_structure.ipynb) | Dispersion plots; distinguishing sustained themes from single episodes | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/10c_dispersion_and_structure.ipynb) |
| [Dispersion as a Statistic: Juilland's D and Gries's DP](10-visualising-and-arguing/10d_dispersion_statistics.ipynb) | Computing dispersion; why DP replaced D; the frequency confound | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/10d_dispersion_statistics.ipynb) |
| [Practice: Build One Figure That Carries an Argument](10-visualising-and-arguing/10e_practice_one_figure.ipynb) | From a defensible finding to a single publishable chart | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/10e_practice_one_figure.ipynb) |
| [From Counts to Argument](10-visualising-and-arguing/11a_from_counts_to_argument.ipynb) | Classifying what a number can carry: description, comparison, claim | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/11a_from_counts_to_argument.ipynb) |
| [What Frequency Cannot Show](10-visualising-and-arguing/11b_what_frequency_cannot_show.ipynb) | The limits section; silence, negation, and who is absent | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/11b_what_frequency_cannot_show.ipynb) |
| [Testing Our Own Findings: The Da Critique](10-visualising-and-arguing/11c_testing_our_own_findings.ipynb) | Permutation tests, resampling, and robustness of a published-style claim | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/11c_testing_our_own_findings.ipynb) |
| [Practice: Turn Counts Into a Paragraph You Can Defend](10-visualising-and-arguing/11d_practice_writing_it_up.ipynb) | Drafting the methods and findings text; hedging that is accurate rather than vague | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/10-visualising-and-arguing/11d_practice_writing_it_up.ipynb) |

### 11-distant-reading-and-its-critics

Culturomics, semantic change, and the Da, Bode and Data Feminism critiques.

| Notebook | Method | Open |
|---|---|---|
| [Counting Across Time, and What the Corpus Is Made Of](11-distant-reading-and-its-critics/22a_culturomics_and_composition.ipynb) | Culturomics; corpus-composition bias; the Ngram Viewer critiques | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/11-distant-reading-and-its-critics/22a_culturomics_and_composition.ipynb) |
| [Semantic Change Without a Neural Network](11-distant-reading-and-its-critics/22b_semantic_change.ipynb) | PPMI vectors and nearest neighbours; how a word's company changes | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/11-distant-reading-and-its-critics/22b_semantic_change.ipynb) |
| [Who Is Missing: Bode, Data Feminism, and the Absence Audit](11-distant-reading-and-its-critics/22c_who_is_missing.ipynb) | Corpus critique as method; auditing what a corpus cannot say | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/11-distant-reading-and-its-critics/22c_who_is_missing.ipynb) |
| [Practice: Audit a Corpus You Intend to Publish On](11-distant-reading-and-its-critics/22d_practice_absence_audit.ipynb) | The five-question absence audit, applied and written up | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/11-distant-reading-and-its-critics/22d_practice_absence_audit.ipynb) |

### 12-neural-foundations

Sequence models and attention, written out rather than imported.

| Notebook | Method | Open |
|---|---|---|
| [Why Word Order Matters, and What Bags of Words Cannot See](12-neural-foundations/24a_why_order_matters.ipynb) | The limits of order-free representations; recurrence as the first fix | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/24a_why_order_matters.ipynb) |
| [Training an LSTM, and Reading Its Limits](12-neural-foundations/24b_lstm_classification.ipynb) | Keras LSTM text classification; comparison against the bag-of-words baseline | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/24b_lstm_classification.ipynb) |
| [Practice: Decide Whether Your Task Needs Sequence](12-neural-foundations/24c_practice_does_order_help.ipynb) | A decision experiment: measure the order signal before buying the model | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/24c_practice_does_order_help.ipynb) |
| [Attention, Written Out in Numpy](12-neural-foundations/25a_attention_from_scratch.ipynb) | Scaled dot-product attention by hand; queries, keys and values | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/25a_attention_from_scratch.ipynb) |
| [Tokenisation: Where African Languages Get Expensive](12-neural-foundations/25b_tokenisation_and_african_languages.ipynb) | Subword tokenisation; fertility and cost across languages | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/25b_tokenisation_and_african_languages.ipynb) |
| [Practice: Budget a Project in Tokens](12-neural-foundations/25c_practice_tokeniser_budget.ipynb) | Costing a real corpus across languages and models before committing | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/12-neural-foundations/25c_practice_tokeniser_budget.ipynb) |

### 13-african-nlp-models

AfriBERTa, AfroXLMR, LaBSE and the MasakhaNER benchmark, scored on held-out data.

| Notebook | Method | Open |
|---|---|---|
| [African NLP Models: What Exists and Who Built It](13-african-nlp-models/23a_african_nlp_models.ipynb) | The AfriBERTa/AfroXLMR/LaBSE landscape; pretrained transfer vs training from scratch | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/23a_african_nlp_models.ipynb) |
| [Cross-Lingual Embeddings: One Meaning, Many Languages](13-african-nlp-models/23b_cross_lingual_embeddings.ipynb) | LaBSE sentence embeddings; cross-lingual retrieval a count-based method cannot do | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/23b_cross_lingual_embeddings.ipynb) |
| [The MasakhaNER Benchmark, Run and Scored](13-african-nlp-models/23c_masakhaner_benchmark.ipynb) | Token classification against gold labels; entity-level evaluation on a real benchmark | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/23c_masakhaner_benchmark.ipynb) |
| [Case Study: Classical and Neural on the Same Task](13-african-nlp-models/23d_classical_vs_neural.ipynb) | Head-to-head comparison; when the extra machinery is worth it | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/23d_classical_vs_neural.ipynb) |
| [Freeze or Fine-Tune: The Decision and Its Cost](13-african-nlp-models/26a_freeze_or_finetune.ipynb) | Frozen features vs full fine-tuning; measuring what adaptation buys | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/26a_freeze_or_finetune.ipynb) |
| [Who the Models Work For](13-african-nlp-models/26b_low_resource_reality.ipynb) | Per-language performance against data volume; measuring the inequity | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/26b_low_resource_reality.ipynb) |
| [Practice: Choose a Model for a Real Project](13-african-nlp-models/26c_practice_choose_your_model.ipynb) | A costed comparison across four workflows on one task | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/13-african-nlp-models/26c_practice_choose_your_model.ipynb) |

### 14-generative-llms

Prompting, hallucination, retrieval-augmented generation and evaluation.

| Notebook | Method | Open |
|---|---|---|
| [Prompting, Decoding, and Confident Wrongness](14-generative-llms/27a_prompting_and_hallucination.ipynb) | Decoding strategies; hallucination on African literary material | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/14-generative-llms/27a_prompting_and_hallucination.ipynb) |
| [Grounding a Model in Your Own Corpus (RAG)](14-generative-llms/27b_rag_grounding.ipynb) | Retrieval-augmented generation over course corpora; citation you can verify | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/14-generative-llms/27b_rag_grounding.ipynb) |
| [Evaluating Generated Text, and Its Circularity](14-generative-llms/27c_evaluating_generated_text.ipynb) | BLEU/ROUGE and their limits; LLM-as-judge and why it is circular | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/14-generative-llms/27c_evaluating_generated_text.ipynb) |
| [Practice: Put an LLM in a Research Pipeline Safely](14-generative-llms/27d_practice_llm_in_a_project.ipynb) | Designing, checking and reporting an LLM-assisted step | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/14-generative-llms/27d_practice_llm_in_a_project.ipynb) |

### 15-the-neural-critique

Interpretability, compute, access, and when not to use any of this.

| Notebook | Method | Open |
|---|---|---|
| [What You Give Up: Interpretability](15-the-neural-critique/28a_interpretability_lost.ipynb) | Coefficients as evidence vs opaque models; what a footnote can cite | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/15-the-neural-critique/28a_interpretability_lost.ipynb) |
| [Compute, Access, and When Not to Use Any of This](15-the-neural-critique/28b_cost_access_and_refusal.ipynb) | Cost and carbon; the stochastic-parrots argument; a decision procedure | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/15-the-neural-critique/28b_cost_access_and_refusal.ipynb) |
| [Practice: Choose the Cheapest Adequate Method](15-the-neural-critique/28c_practice_method_decision.ipynb) | Applying the six-step decision procedure to real questions | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/15-the-neural-critique/28c_practice_method_decision.ipynb) |

### 16-case-studies

One real project audited end to end, including the mistake that inflated its result by 24 points.

| Notebook | Method | Open |
|---|---|---|
| [A Neural Pipeline on 61 African Novels](16-case-studies/13a_the_case.ipynb) | Reading a real project: architecture, corpus, and what it claimed | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/16-case-studies/13a_the_case.ipynb) |
| [The Split That Inflated the Result by 24 Points](16-case-studies/13b_the_leak.ipynb) | Group leakage; why a random split flatters an authorship model | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/16-case-studies/13b_the_leak.ipynb) |
| [The Corpus We Cannot Ship](16-case-studies/13c_the_corpus_we_cannot_ship.ipynb) | Copyright, redistribution and reproducibility as method constraints | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/16-case-studies/13c_the_corpus_we_cannot_ship.ipynb) |
| [The Same Pipeline, on Text We Can Share](16-case-studies/13d_the_pipeline_on_clean_text.ipynb) | Reproducing the case study's six steps end to end in Keras | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/16-case-studies/13d_the_pipeline_on_clean_text.ipynb) |

### 17-capstone

The whole workflow, on a corpus and question of your own.

| Notebook | Method | Open |
|---|---|---|
| [Capstone: A Complete Analysis](17-capstone/12_capstone.ipynb) | The whole workflow, on a corpus and question of your own | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sagaustus/adh-dh-notebooks/blob/main/17-capstone/12_capstone.ipynb) |

## How these were built

Generated from one source of truth in the CourseHub repository, so the Colab notebooks and the in-browser lessons cannot drift apart. Every notebook is executed end to end as part of the build.

```
python colab_pack/build_pack.py --pack text --check
python colab_pack/test_notebooks.py --pack text --jobs 4
```

## Licence

Notebooks CC BY 4.0. Corpora keep their own licences, listed above and in `PROVENANCE.md`.

