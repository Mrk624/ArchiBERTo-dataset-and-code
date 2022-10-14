# ArchiBERTo a Multi-label Classifier in Italian Design and Construction knowledge domain

ArchiBERTo is developed to process and translate the quality objectives expressed in a Documento di Indirizzo alla Progettazione (DIP) into a ranking of criteria and objectives, which represent the computational counterpart of the natural language information, the Text Classification task was identified as the most suitable to achieve the goal. Among the Text Classification tasks, the Multi-label Text Classification (MTC) is selected. MTC is a text analysis technique that automatically applies one or more predefined classification labels to a single text or sentence. Unlike common classification tasks, in which class labels are mutually exclusive, multi-label classification allows predicting and assigning multiple mutually non-exclusive classes, i.e., a list of predefined labels which represents the appointing party quality objectives and demands. ArchiBERTo is then developed having the the capability to perform a multi-label classification to automatically process and translate the needs expressed in a DIP document into a ranking of quality objectives/criteria.

Bidirectional Encoder Representation from Transformers (BERT) language model, a pre-trained context-aware language model, and the transfer-learning technique are identified as the most suitable approaches to develop the NLP tool ArchiBERTo. BERT-based algorithms are the state of the art in the NLP field, allowing the same pre-trained model to successfully tackle a broad set of NLP tasks.

Consequently, the NLP tool ArchiBERTo is trained to classify sentences by assigning multiple previously defined labels to natural language expressions. The main activities to develop the tool are listed below and briefly explained:

•	labels definition: for the selected case study, a list of predefined labels, defined by the appointing party, is already available. The labels definition is the result of a cooperation among different experts and end-users (i.e., architects, designers, pedagogues, agronomists, and citizens) who represent the appointing party quality objectives and needs.

•	training and validation Dataset production: a Dataset is defined and then is randomly split into a training and validation Datasets at a 0.8:0.2 ratio:
  o	a training Dataset for the fine-tuning activity, which is used to further train the BERT model, basically the model learns from this data;
  o	a validation Dataset to evaluate the performances of the trained model, it is the sample of data used to provide an unbiased evaluation of the model.
  
The production of the general Dataset is the result of a collaboration between experts, with knowledge in the architectural, design, and construction fields. Moreover, to avoid any bias in the production of the Dataset, a labelling procedure has been defined: each expert is asked to independently propose a hypothesis for the labelling of each sentence, after that the experts share their hypothesis and in case of disagreement on some labels, they are asked to share the motivation of their label choices and converge on a single common proposal. In fact, the construction of the Dataset by different experts, following the described procedure, allows the model to represent and use the experts’ collective knowledge in the labelling activity. By representing a collective intelligence of a group of people, larger than the ability of a single expert to judge and classify quality objectives related sentences, the NLP tool aims to avoid subjectivity in the interpretation of textual information. ArchiBERTo aims to outperform the capability of a single expert to manage the complexity of analyzing several sentences being the representation of the group of experts’ knowledge.

•	model fine-tuning: once defined the Dataset, to properly train the BERT model, a set of hyperparameters are defined. Hyperparameters are a variable configuration external to the model and whose values cannot be estimated from the data are defined via a trial and errors cycle.

•	performance assessment metrics: to measure the NLP tool accuracy, the model predictions are compared with the human annotation, considered as the best standard, and the F1-score metric is selected to measure the tool accuracy. Training and Validation loss curves are also plotted and analyzed to avoid underfitting or overfitting phenomena.

The .ipynb code of the Jupyter notebook and the Training and Validation Dataset produced and used in the development of ArchiBERTo are available.


