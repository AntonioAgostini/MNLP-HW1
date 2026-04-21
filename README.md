# MNLP-HW1

In this readme, we specify the meaning of each jsonl output file.

- FT-InB: Finetuned using In-Batch negatives
- FT-HN: Finetuned using Hard Negatives
- CE-RR: Finetuned using a CrossEncoder as a ReRanker

We refer to the models with one of the above name to be coherent with the report and the colab notebook.

----------------------------------------------------------
FT-InB: 

`TheOverfitters-test-distilbert_base_uncased-FT_InB.jsonl`
`TheOverfitters-blind-distilbert_base_uncased-FT_InB.jsonl`

contain the requested output for both the test and the blind set for the model finetuned with in-batch negatives, where in sample negatives
were picked from the candidate chunks set of the current query for the training tuple (anchor, pos, neg_1, neg_2, neg_3). 
----------------------------------------------------------
FT-HN: 

`TheOverfitters-test-distilbert_base_uncased-FT_HN.jsonl`
`TheOverfitters-blind-distilbert_base_uncased-FT_HN.jsonl`

contain the requested output for both the test and the blind set for the model finetuned with explicit hard negatives, where in sample negatives
were picked from the top k = 5 items chosen by the model FT-InB.
----------------------------------------------------------
CE-RR: 

`TheOverfitters-test-distilbert_base_uncased-CE_RR.jsonl`
`TheOverfitters-blind-distilbert_base_uncased-CE_RR.jsonl`

contain the requested output for both the test and the blind set for the model finetuned with explicit hard negatives + reranker.
----------------------------------------------------------
