# etymo-10k


| Name         | Description  |
| -------------| :-----|
| `papers.json`     | Paper metadata  |
| `keywords.json` | Automatically extracted keywords from paper full text |
| `similarity-based-graph-tfidf.gexf`    |  Content similarity network (TFIDF based) |
| `keyword-graphs` | A group of keyword graphs at different timestamps |


In details:

* `papers.json`: a list of papers, each contains the following information:
  - `paper_id`: paper id
  - `abstract`: paper abstract
  - `authors`: list of author names
  - `category_name`
  - `doi`
  - `downloaded_date`: downloaded date
  - `journal_name`: journal name
  - `link`: paper abstract URL
  - `pdf_link`: link to paper PDF
  - `overall_score`: overall importance score
  - `pagerank`: PageRank score
  - `reverse_pagerank`: reverse PageRank score
  - `published_date`: published date
  - `related_papers`: related paper ids
  - `stars`: number of stars (default 0)
  - `tags`: paper tags
  - `title`
  - `type_name`: `paper`

  For example,
  ```
  {'abstract': 'Neuroscience research has produced many theories and computational neural\nmodels of sensory nervous systems. Notwithstanding many different perspectives\ntowards developing intelligent machines, artificial intelligence has ultimately\nbeen influenced by neuroscience. Therefore, this paper provides an introduction\nto biologically inspired machine intelligence by exploring the basic principles\nof sensation and perception as well as the structure and behavior of biological\nsensory nervous systems like the neocortex. Concepts like spike timing,\nsynaptic plasticity, inhibition, neural structure, and neural behavior are\napplied to a new model, Simple Cortex (SC). A software implementation of SC has\nbeen built and demonstrates fast observation, learning, and prediction of\nspatio-temporal sensory-motor patterns and sequences. Finally, this paper\nsuggests future areas of improvement and growth for Simple Cortex and other\nrelated machine intelligence models.',
   'authors': [{'name': 'David Di Giorgio'}],
   'category_name': 'uncategorised',
   'doi': '',
   'downloaded_date': '2018-05-21T12:52:44.577330',
   'journal_name': 'arXiv:cs.AI',
   'link': 'http://arxiv.org/abs/1710.01347v1',
   'overall_score': 0.000137021,
   'pagerank': 1.67701e-05,
   'paper_id': 29477,
   'pdf_link': 'http://arxiv.org/pdf/1710.01347v1',
   'published_date': '2017-10-03T00:00:00',
   'related_papers': [29746,
    29609,
    29898,
    29566,
    29782,
    29820,
    29478,
    29876,
    29639,
    29713,
    29897,
    29726,
    29944],
   'reverse_pagerank': 0.000618026,
   'stars': 0,
   'tags': None,
   'title': 'Simple Cortex: A Model of Cells in the Sensory Nervous System',
   'type_name': 'paper'}
  ```

* `keywords.json`: extracted keywords from each paper.
  - `paper_id`: paper id
  - `keywords`: a list of keywords. Each keyword key has three values: RAKE score, term frequency, and (Inverse Document Frequency) IDF score.

* `keyword-graphs`: nodes are keywords and related keywords are connected by edges. `keyword-graphs` is a folder that contains keyword graphs at different time stamps. For example `graph.2017.10.gexf` represents a keyword graph at time stamp year `2017` and month `10`.
