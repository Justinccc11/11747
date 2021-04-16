For our baseline reproduction, we tried to reproduce the results from
bert_joint, bartNQ(included in unifiedQA), and unifiedQA using the cloned repo
bert_joint from google-research/language inside experimnets_for_bert_joint 
and the unifiedQA repo inside experiments_for_unified_QA. We also tried DPR, a retriever
+ reader framework, however due to computational limits, we were not able to train
the retriever and obtain embedding for paragraphs: the authors used 8x 32GB GPUs and
  trained for a few days, and for unifiedQA, we were not able to replicate the experiment
  exactly, as we had to lower the batchsize and finetune for fewer epoches given that we
  only have a 16GB P100 GPU to work with on colab and a 12GB GPU from aws p2x.large instance.