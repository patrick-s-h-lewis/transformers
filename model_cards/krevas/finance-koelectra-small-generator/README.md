---
language: korean
---

# 📈 Financial Korean ELECTRA model

Pretrained ELECTRA Language Model for Korean (`finance-koelectra-small-generator`)

> ELECTRA is a new method for self-supervised language representation learning. It can be used to
> pre-train transformer networks using relatively little compute. ELECTRA models are trained to
> distinguish "real" input tokens vs "fake" input tokens generated by another neural network, similar to
> the discriminator of a GAN.

More details about ELECTRA can be found in the [ICLR paper](https://openreview.net/forum?id=r1xMH1BtvB)
or in the [official ELECTRA repository](https://github.com/google-research/electra) on GitHub.

## Stats

The current version of the model is trained on a financial news data of Naver news.

The final training corpus has a size of 25GB and 2.3B tokens.

This model was trained a cased model on a TITAN RTX for 500k steps.

## Usage

```python
from transformers import pipeline

fill_mask = pipeline(
            "fill-mask",
            model="krevas/finance-koelectra-small-generator",
            tokenizer="krevas/finance-koelectra-small-generator"
            )

print(fill_mask(f"내일 해당 종목이 대폭 {fill_mask.tokenizer.mask_token}할 것이다."))
```

# Huggingface model hub

All models are available on the [Huggingface model hub](https://huggingface.co/krevas).