# Classification With BERT

After the project on Fine Tuning, it is time for some action. We put all those learnings in fine-tuning a known Transformer model for a specific task.

We will be fine-tuning a BERT (Bidirectional Encoder Representations from Transformers) model for a simple classification task. This will be our first encounter with working with a Transformer model.

The BERT model we will work is going to be the [base model](https://huggingface.co/google-bert/bert-base-uncased?text=He+is+my+%5BMASK%5D.), google-bert/bert-base-uncased. It has about 110M parameters. It is based on the [paper](https://arxiv.org/pdf/1810.04805.pdf).

In particular, we will fine-tune the BERT model on a [Fake News](https://www.kaggle.com/datasets/iamrahulthorat/fakenews-csv/data) dataset. We do this in 3 different ways.

1) Freezing the entire model and training only its last layer.
2) Freezing the entire model and adding another layer at its end and then training them.
3) Training the entire model.

We find that the accuracies that we get from these models are in increasing order as stated above, and this was also expected. Although, fine-tuning the entire model took a longer time than partial training.
