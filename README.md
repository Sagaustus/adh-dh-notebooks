<!-- BEGIN GENERATED -->
# Computational Text Analysis Pack

Computational text analysis for African digital humanities. One notebook per
method, where **one row is a document, a passage or a word** rather than a
spreadsheet cell. Built for scholars of literature, languages and linguistics
who want the statistics behind the tools.

## Using them

Each notebook is self-contained — open any one without having run the others.

**In Google Colab:** click the badge at the top of a notebook and run the
first cell. It downloads the corpora it needs from CourseHub — no upload,
no login. If that server is unreachable it falls back to asking you to
upload them from this pack's `data/` folder.

**Locally:** put the notebook in the same folder as the CSVs and run it.
Needs `pandas`, `numpy`, `matplotlib`, `scipy`, `scikit-learn`, `statsmodels`.

**Inside CourseHub:** every notebook is also the 📓 Lab Notebook tab on its
lesson, next to the quiz. Nothing to install and no upload step.

## Data

Real African-language and African-archive text. News in 16 African languages
with topic labels, passages from 150 public-domain works about Africa, and
passages from 48 African court judgments and government reports.
Everything is public domain, open government, or AFL-3.0. Nothing in-copyright
is included. See `data/PROVENANCE.md`.

| File | What it is |
|---|---|
| `masakhanews.csv` | news in 16 African languages with topic labels; 3,600 of the 8,400 documents are in Hausa, Igbo, Yoruba or Nigerian Pidgin |
| `masakhaner.csv` |  |
| `colonial_texts.csv` | 5,984 passages from 150 public-domain works about Africa — a colonial-discourse corpus, not an African-authored one |
| `african_legal.csv` | 1,692 passages from 48 African court judgments and government reports |

## The notebooks

| # | Notebook | Technique |
|---|---|---|
| | **Module 00 — Text as Data** | |
| `00` | [Text as Data](notebooks/00_text_as_data.ipynb) | Turning a corpus into a table: document, token, type |
| | **Module 01 — Framing the Question** | |
| `01a` | [What a Corpus Can and Cannot Answer](notebooks/01a_what_a_corpus_answers.ipynb) | Matching a literary or linguistic question to a countable method |
| `01b` | [Whose Africa Is in the Public Domain?](notebooks/01b_whose_africa_is_public_domain.ipynb) | Corpus construction as an argument; the absence audit for text |
| | **Module 02 — Describing a Corpus** | |
| `02a` | [Word Frequency](notebooks/02a_word_frequency.ipynb) | Frequency distributions; raw counts vs normalised rates |
| `02b` | [Zipf's Law](notebooks/02b_zipfs_law.ipynb) | Rank-frequency distributions; the long tail and what it costs you |
| `02c` | [Type/Token Ratio and Its Trap](notebooks/02c_type_token_ratio.ipynb) | Vocabulary richness; length dependence and standardised TTR |
| `02d` | [Document Length as Evidence](notebooks/02d_document_length.ipynb) | Distributions of length; median vs mean; when a skew is the finding |
| | **Module 03 — Preparing Text** | |
| `03a` | [Stopwords Are Not Universal](notebooks/03a_stopwords_are_not_universal.ipynb) | Stopword removal; why English lists do nothing to African languages |
| `03b` | [Diacritics and the ASCII Trap](notebooks/03b_diacritics_and_the_ascii_trap.ipynb) | Unicode-aware tokenising; measuring what naive cleaning destroys |
| | **Module 04 — Comparing Corpora** | |
| `04a` | [Keyness: Which Words Distinguish a Corpus](notebooks/04a_keyness.ipynb) | Log-likelihood keyness; target vs reference corpus |
| `04b` | [Effect Size for Words](notebooks/04b_effect_size_for_words.ipynb) | Why significance is not importance; log ratio and %DIFF |
| `04c` | [Comparing Across Archives](notebooks/04c_comparing_across_archives.ipynb) | Keyness between unlike corpora; confounds you cannot remove |
| | **Module 05 — Concordance and Collocation** | |
| `05a` | [KWIC: Reading What a Count Points At](notebooks/05a_kwic_concordance.ipynb) | Keyword-in-context; using a count to direct close reading |
| `05b` | [Collocation: The Company a Word Keeps](notebooks/05b_collocation.ipynb) | Window co-occurrence; span and its effect on results |
| `05c` | [Association Measures: PMI, Dice and Log-Likelihood](notebooks/05c_association_measures.ipynb) | Choosing an association statistic and knowing what it favours |
| | **Module 06 — Clustering Documents** | |
| `06a` | [Vectorising Text: TF-IDF](notebooks/06a_vectorising_text.ipynb) | Document–term matrices; term weighting and what min_df does |
| `06b` | [Clustering Documents with K-Means](notebooks/06b_clustering_documents.ipynb) | K-means on TF-IDF; choosing k and reading clusters honestly |
| `06c` | [Dendrograms: Clustering Without Choosing K](notebooks/06c_dendrograms.ipynb) | Hierarchical clustering; linkage choice and cutting the tree |
| | **Module 07 — Classification** | |
| `07a` | [Train and Test: The Split That Makes a Number Mean Something](notebooks/07a_train_test_on_text.ipynb) | Held-out evaluation; leakage; the majority-class baseline |
| `07b` | [Features and Models: What Actually Moves the Number](notebooks/07b_features_and_models.ipynb) | Comparing feature settings and classifiers; cross-validation |
| `07c` | [Which Words Carry the Decision](notebooks/07c_which_words_carry_the_decision.ipynb) | Model coefficients as evidence; interpreting a linear classifier |
| | **Module 08 — Topic Modelling** | |
| `08a` | [Topic Modelling with LDA](notebooks/08a_topic_modelling_lda.ipynb) | Latent Dirichlet Allocation; documents as mixtures of topics |
| `08b` | [NMF: The Other Topic Model](notebooks/08b_nmf_topics.ipynb) | Non-negative matrix factorisation; comparing two models on one corpus |
| `08c` | [Reading Topics Sceptically](notebooks/08c_reading_topics_sceptically.ipynb) | Choosing k; coherence; the topics that are artefacts |
| | **Module 09 — Stylometry** | |
| `09a` | [Most-Frequent Words: The Signal Everyone Discards](notebooks/09a_most_frequent_words.ipynb) | MFW feature sets; why function words identify authors |
| `09b` | [Burrows's Delta](notebooks/09b_burrows_delta.ipynb) | Z-scored MFW plus a distance measure; the standard attribution method |
| `09c` | [Style Beyond Authorship](notebooks/09c_style_beyond_authorship.ipynb) | Stylometric features for genre, register and translation |
| | **Module 10 — Visualising Text** | |
| `10a` | [Charting Frequency and Difference](notebooks/10a_charting_frequency.ipynb) | Bar charts, ranked comparisons, and the axis decisions that mislead |
| `10b` | [Why Word Clouds Mislead](notebooks/10b_why_word_clouds_mislead.ipynb) | Diagnosing a visualisation; area perception and the alternatives |
| `10c` | [Dispersion: Where in a Text a Word Appears](notebooks/10c_dispersion_and_structure.ipynb) | Dispersion plots; distinguishing sustained themes from single episodes |
| | **Module 11 — From Counts to Argument** | |
| `11a` | [From Counts to Argument](notebooks/11a_from_counts_to_argument.ipynb) | Classifying what a number can carry: description, comparison, claim |
| `11b` | [What Frequency Cannot Show](notebooks/11b_what_frequency_cannot_show.ipynb) | The limits section; silence, negation, and who is absent |
| | **Module 12 — Capstone** | |
| `12` | [Capstone: A Complete Analysis](notebooks/12_capstone.ipynb) | The whole workflow, on a corpus and question of your own |
| | **Module 02 — Describing a Corpus** | |
| `02e` | [Vocabulary Richness Beyond TTR](notebooks/02e_vocabulary_richness.ipynb) | Yule's K, Herdan's C, MATTR and Heaps's law; length-robust richness |
| | **Module 04 — Comparing Corpora** | |
| `04d` | [Why Significance Stops Meaning Anything](notebooks/04d_significance_and_its_critics.ipynb) | The Kilgarriff/Gries/Koplenig debate, demonstrated by resampling |
| | **Module 05 — Concordance and Collocation** | |
| `05d` | [t-score, log-Dice and Delta P](notebooks/05d_association_measures_completed.ipynb) | The association measures the field actually reports, and their biases |
| | **Module 08 — Topic Modelling** | |
| `08d` | [Are Topics Evidence? Coherence and Its Critics](notebooks/08d_are_topics_evidence.ipynb) | NPMI coherence; Chang's 'reading tea leaves'; Schmidt's 'Words Alone' |
| | **Module 09 — Stylometry** | |
| `09d` | [Delta Variants: Cosine, Eder, and the MFW Question](notebooks/09d_delta_variants.ipynb) | Comparing Delta measures and MFW bands; bootstrap consensus trees |
| `09e` | [Zeta and Character N-grams](notebooks/09e_zeta_and_character_ngrams.ipynb) | Craig's Zeta on mid-frequency words; character n-gram attribution |
| | **Module 10 — Visualising Text** | |
| `10d` | [Dispersion as a Statistic: Juilland's D and Gries's DP](notebooks/10d_dispersion_statistics.ipynb) | Computing dispersion; why DP replaced D; the frequency confound |
| | **Module 11 — From Counts to Argument** | |
| `11c` | [Testing Our Own Findings: The Da Critique](notebooks/11c_testing_our_own_findings.ipynb) | Permutation tests, resampling, and robustness of a published-style claim |
| | **Module 06 — Clustering Documents** | |
| `06d` | [LSA and LSI: Where Document Vectors Came From](notebooks/06d_lsa_and_the_vector_lineage.ipynb) | Truncated SVD on a term-document matrix; the ancestor of embeddings |
| | **Module 09 — Stylometry** | |
| `09f` | [Mosteller and Wallace: The Federalist Papers](notebooks/09f_mosteller_and_wallace.ipynb) | The founding authorship study; Bayesian reasoning on function words |
| | **Module 13 — Case Studies** | |
| `13a` | [A Neural Pipeline on 61 African Novels](notebooks/13a_the_case.ipynb) | Reading a real project: architecture, corpus, and what it claimed |
| `13b` | [The Split That Inflated the Result by 24 Points](notebooks/13b_the_leak.ipynb) | Group leakage; why a random split flatters an authorship model |
| `13c` | [The Corpus We Cannot Ship](notebooks/13c_the_corpus_we_cannot_ship.ipynb) | Copyright, redistribution and reproducibility as method constraints |
| `13d` | [The Same Pipeline, on Text We Can Share](notebooks/13d_the_pipeline_on_clean_text.ipynb) | Reproducing the case study's six steps end to end in Keras |
| | **Module 14 — Preparing Text, Properly** | |
| `14a` | [Stemming, Lemmatisation, and Why Preprocessing Is Not Neutral](notebooks/14a_stemming_and_lemmatisation.ipynb) | Suffix stripping vs dictionary lookup; Schofield & Mimno's warning |
| `14b` | [Finite-State Morphology: Rules That Run Both Ways](notebooks/14b_finite_state_morphology.ipynb) | Two-level morphology; a reversible analyser/generator for Swahili verbs |
| `14c` | [Historical Spelling and Orthographic Normalisation](notebooks/14c_historical_normalisation.ipynb) | Edit distance, phonetic matching and rewrite rules; the VARD/Norma approach |
| `14d` | [OCR Error and How It Propagates](notebooks/14d_ocr_error_propagation.ipynb) | Character error rate; measuring the downstream cost of noisy text |
| | **Module 15 — Rule-Based and Symbolic Methods** | |
| `15a` | [Regular Expressions as Scholarly Method](notebooks/15a_regex_as_method.ipynb) | Pattern extraction as evidence; precision, recall and the Unicode trap |
| `15b` | [A Corpus Query Language of Your Own](notebooks/15b_corpus_query_language.ipynb) | CQL/CQP semantics; querying token sequences rather than characters |
| `15c` | [Gazetteers and Rule-Based Extraction](notebooks/15c_gazetteers_and_rules.ipynb) | ANNIE/JAPE-style entity extraction; when rules beat statistical NER |
| `15d` | [Dictionary-Based Content Analysis and Its Limits](notebooks/15d_dictionary_content_analysis.ipynb) | General Inquirer-style category counting; why sentiment lexicons fail here |
| | **Module 16 — Sequence Labelling** | |
| `16a` | [Tagging a Sequence: Hidden Markov Models and Viterbi](notebooks/16a_hmm_pos_tagging.ipynb) | HMM tagging from scratch; emission and transition probabilities; Viterbi |
| `16b` | [Features, Not Just Words: Toward CRFs](notebooks/16b_features_and_crfs.ipynb) | Feature engineering for sequence models; why CRFs replaced HMMs |
| | **Module 17 — Annotation and Agreement** | |
| `17a` | [Coding a Corpus, and Cohen's Kappa](notebooks/17a_coding_and_cohens_kappa.ipynb) | Coding schemes; raw agreement vs chance-corrected agreement |
| `17b` | [Krippendorff's Alpha: Agreement That Generalises](notebooks/17b_krippendorffs_alpha.ipynb) | Alpha for any number of coders, missing data and measurement levels |
| | **Module 18 — Text Reuse and Intertextuality** | |
| `18a` | [Shingling: Finding Reuse Without Reading](notebooks/18a_shingling_and_jaccard.ipynb) | Character and word shingles; Jaccard similarity; the quadratic wall |
| `18b` | [MinHash and LSH: Reuse Detection That Scales](notebooks/18b_minhash_and_lsh.ipynb) | Signature sketching and locality-sensitive hashing; sub-quadratic search |
| `18c` | [Aligning Reuse, and Reading What Changed](notebooks/18c_aligning_and_reading_reuse.ipynb) | Sequence alignment on detected pairs; editing as evidence |
| | **Module 19 — Networks from Text** | |
| `19a` | [Collocation Networks](notebooks/19a_collocation_networks.ipynb) | Building and reading a GraphColl-style collocation network |
| `19b` | [Character and Entity Networks](notebooks/19b_character_networks.ipynb) | Co-occurrence networks of people; Moretti's plot networks and their critics |
| | **Module 20 — Encoding as Method** | |
| `20a` | [TEI-XML: Encoding Is Interpretation](notebooks/20a_tei_and_what_markup_asserts.ipynb) | TEI P5 structure; markup as a scholarly claim rather than formatting |
| `20b` | [Querying TEI with XPath](notebooks/20b_querying_tei_with_xpath.ipynb) | XPath over encoded text; structural queries a plain-text search cannot make |
| `20c` | [Standoff Annotation and CoNLL-U](notebooks/20c_standoff_and_conllu.ipynb) | Character-offset annotation; overlapping hierarchies; interchange formats |
| | **Module 21 — The Lineage** | |
| `21a` | [Busa, the Concordance, and Where All This Came From](notebooks/21a_busa_and_the_concordance.ipynb) | Index verborum and KWIC as the founding method; reconstructing the workflow |
| | **Module 22 — Distant Reading and Its Critics** | |
| `22a` | [Counting Across Time, and What the Corpus Is Made Of](notebooks/22a_culturomics_and_composition.ipynb) | Culturomics; corpus-composition bias; the Ngram Viewer critiques |
| `22b` | [Semantic Change Without a Neural Network](notebooks/22b_semantic_change.ipynb) | PPMI vectors and nearest neighbours; how a word's company changes |
| `22c` | [Who Is Missing: Bode, Data Feminism, and the Absence Audit](notebooks/22c_who_is_missing.ipynb) | Corpus critique as method; auditing what a corpus cannot say |
| | **Module 23 — African NLP Models and Benchmarks** | |
| `23a` | [African NLP Models: What Exists and Who Built It](notebooks/23a_african_nlp_models.ipynb) | The AfriBERTa/AfroXLMR/LaBSE landscape; pretrained transfer vs training from scratch |
| `23b` | [Cross-Lingual Embeddings: One Meaning, Many Languages](notebooks/23b_cross_lingual_embeddings.ipynb) | LaBSE sentence embeddings; cross-lingual retrieval a count-based method cannot do |
| `23c` | [The MasakhaNER Benchmark, Run and Scored](notebooks/23c_masakhaner_benchmark.ipynb) | Token classification against gold labels; entity-level evaluation on a real benchmark |
| `23d` | [Case Study: Classical and Neural on the Same Task](notebooks/23d_classical_vs_neural.ipynb) | Head-to-head comparison; when the extra machinery is worth it |
| | **Module 24 — Sequence Models** | |
| `24a` | [Why Word Order Matters, and What Bags of Words Cannot See](notebooks/24a_why_order_matters.ipynb) | The limits of order-free representations; recurrence as the first fix |
| `24b` | [Training an LSTM, and Reading Its Limits](notebooks/24b_lstm_classification.ipynb) | Keras LSTM text classification; comparison against the bag-of-words baseline |
| | **Module 25 — Transformers and Attention** | |
| `25a` | [Attention, Written Out in Numpy](notebooks/25a_attention_from_scratch.ipynb) | Scaled dot-product attention by hand; queries, keys and values |
| `25b` | [Tokenisation: Where African Languages Get Expensive](notebooks/25b_tokenisation_and_african_languages.ipynb) | Subword tokenisation; fertility and cost across languages |
| | **Module 26 — Fine-Tuning Pretrained Models** | |
| `26a` | [Freeze or Fine-Tune: The Decision and Its Cost](notebooks/26a_freeze_or_finetune.ipynb) | Frozen features vs full fine-tuning; measuring what adaptation buys |
| `26b` | [Who the Models Work For](notebooks/26b_low_resource_reality.ipynb) | Per-language performance against data volume; measuring the inequity |
| | **Module 28 — The Neural Critique** | |
| `28a` | [What You Give Up: Interpretability](notebooks/28a_interpretability_lost.ipynb) | Coefficients as evidence vs opaque models; what a footnote can cite |
| `28b` | [Compute, Access, and When Not to Use Any of This](notebooks/28b_cost_access_and_refusal.ipynb) | Cost and carbon; the stochastic-parrots argument; a decision procedure |
| | **Module 27 — Generative Models in DH Research** | |
| `27a` | [Prompting, Decoding, and Confident Wrongness](notebooks/27a_prompting_and_hallucination.ipynb) | Decoding strategies; hallucination on African literary material |
| `27b` | [Grounding a Model in Your Own Corpus (RAG)](notebooks/27b_rag_grounding.ipynb) | Retrieval-augmented generation over course corpora; citation you can verify |
| `27c` | [Evaluating Generated Text, and Its Circularity](notebooks/27c_evaluating_generated_text.ipynb) | BLEU/ROUGE and their limits; LLM-as-judge and why it is circular |
| | **Module 02 — Describing a Corpus** | |
| `02f` | [Practice: Does Nigerian-Language News Look Different?](notebooks/02f_practice_describing.ipynb) | A description worked end to end: length, richness, and what they license |
| | **Module 03 — Preparing Text** | |
| `03c` | [Practice: How Much Does Preprocessing Change Your Result?](notebooks/03c_practice_preprocessing.ipynb) | One finding, five preprocessing pipelines, and the spread between them |
| | **Module 04 — Comparing Corpora** | |
| `04e` | [Practice: What Distinguishes Health Coverage, Robustly?](notebooks/04e_practice_comparing.ipynb) | Keyness with effect size, dispersion and a robustness check, end to end |
| | **Module 05 — Concordance and Collocation** | |
| `05e` | [Practice: What Company Does 'Government' Keep?](notebooks/05e_practice_collocation.ipynb) | Collocation to concordance and back; a reading grounded in counts |
| | **Module 06 — Clustering Documents** | |
| `06e` | [Practice: Does This Corpus Cluster by Topic or by Language?](notebooks/06e_practice_clustering.ipynb) | Unsupervised structure, and testing what the clusters actually track |
| | **Module 07 — Classification** | |
| `07d` | [Practice: Build a Classifier You Could Defend](notebooks/07d_practice_classifier.ipynb) | A supervised study end to end: baseline, model, errors, and honest reporting |
| | **Module 08 — Topic Modelling** | |
| `08e` | [Practice: Are These Topics Worth Reporting?](notebooks/08e_practice_topics.ipynb) | A topic model from k-selection to a defensible written interpretation |
| | **Module 09 — Stylometry** | |
| `09g` | [Practice: Attribute an Anonymous Work](notebooks/09g_practice_attribution.ipynb) | A full attribution study, with the checks that make it publishable |
| | **Module 10 — Visualising Text** | |
| `10e` | [Practice: Build One Figure That Carries an Argument](notebooks/10e_practice_one_figure.ipynb) | From a defensible finding to a single publishable chart |
| | **Module 11 — From Counts to Argument** | |
| `11d` | [Practice: Turn Counts Into a Paragraph You Can Defend](notebooks/11d_practice_writing_it_up.ipynb) | Drafting the methods and findings text; hedging that is accurate rather than vague |
| | **Module 14 — Preparing Text, Properly** | |
| `14e` | [Practice: Audit a Preparation Pipeline End to End](notebooks/14e_practice_pipeline_audit.ipynb) | Tracing one document through every preparation step and costing each |
| | **Module 15 — Rule-Based and Symbolic Methods** | |
| `15e` | [Practice: Extract an Entity Type With No Training Data](notebooks/15e_practice_rules_vs_stats.ipynb) | Building, measuring and iterating a rule set against a hand-checked sample |
| | **Module 16 — Sequence Labelling** | |
| `16c` | [Practice: Is an Off-the-Shelf Tagger Good Enough for Your Corpus?](notebooks/16c_practice_tagging_project.ipynb) | Evaluating a tagger on your own material before depending on it |
| | **Module 17 — Annotation and Agreement** | |
| `17c` | [Practice: Build a Coding Scheme and Test It](notebooks/17c_practice_coding_scheme.ipynb) | From category definitions to a measured agreement figure |
| | **Module 18 — Text Reuse and Intertextuality** | |
| `18d` | [Practice: Trace a Story Across a Corpus](notebooks/18d_practice_reuse_study.ipynb) | Detection, filtering, clustering and the direction problem |
| | **Module 19 — Networks from Text** | |
| `19c` | [Practice: Make a Network Claim You Can Defend](notebooks/19c_practice_network_argument.ipynb) | Building a network, testing its stability, and stating what it shows |
| | **Module 20 — Encoding as Method** | |
| `20d` | [Practice: Encode One Page, and Argue With Yourself](notebooks/20d_practice_encode_a_page.ipynb) | A full TEI encoding decision log, and querying what you asserted |
| | **Module 21 — The Lineage** | |
| `21b` | [Practice: Build the Instrument Busa Built](notebooks/21b_practice_build_a_concordance.ipynb) | A complete index verborum and concordance, then a reading from it |
| | **Module 22 — Distant Reading and Its Critics** | |
| `22d` | [Practice: Audit a Corpus You Intend to Publish On](notebooks/22d_practice_absence_audit.ipynb) | The five-question absence audit, applied and written up |
| | **Module 24 — Sequence Models** | |
| `24c` | [Practice: Decide Whether Your Task Needs Sequence](notebooks/24c_practice_does_order_help.ipynb) | A decision experiment: measure the order signal before buying the model |
| | **Module 25 — Transformers and Attention** | |
| `25c` | [Practice: Budget a Project in Tokens](notebooks/25c_practice_tokeniser_budget.ipynb) | Costing a real corpus across languages and models before committing |
| | **Module 00 — Text as Data** | |
| `00b` | [Practice: Your First Hour With an Unfamiliar Corpus](notebooks/00b_practice_first_look.ipynb) | A reproducible first-look protocol before any analysis |
| | **Module 01 — Framing the Question** | |
| `01c` | [Practice: Match Your Question to a Method](notebooks/01c_practice_match_question.ipynb) | Turning a humanities question into a countable one, or deciding it is not |
| | **Module 26 — Fine-Tuning Pretrained Models** | |
| `26c` | [Practice: Choose a Model for a Real Project](notebooks/26c_practice_choose_your_model.ipynb) | A costed comparison across four workflows on one task |
| | **Module 27 — Generative Models in DH Research** | |
| `27d` | [Practice: Put an LLM in a Research Pipeline Safely](notebooks/27d_practice_llm_in_a_project.ipynb) | Designing, checking and reporting an LLM-assisted step |
| | **Module 28 — The Neural Critique** | |
| `28c` | [Practice: Choose the Cheapest Adequate Method](notebooks/28c_practice_method_decision.ipynb) | Applying the six-step decision procedure to real questions |

## Rebuilding

Notebooks are generated from `colab_pack/` in the coursehub repo.
Edit the content modules there, not the `.ipynb` files:

```bash
python colab_pack/build_pack.py --pack text --check --zip
```

Every notebook is executed end to end as part of the build, so the worked
answers are known to reproduce the figures quoted in the course.

<!-- END GENERATED -->
