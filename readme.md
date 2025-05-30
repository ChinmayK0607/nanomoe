

Please run `data.py` in the `trainers` folder first in the same directory where the training code lives.

Sample usage:
```
python train_muon.py --experiment_name muon
```

For logging:

```
python logger.py --experiment_name muon
```

Sample for profiling:

```
python train_muon.py --experiment_name muon --enable_profiling
```

# About

This repo is an attempt to port all changes of nanogpt modded by Keller Jordan to MoE(Mixture of Experts) architecture


GitHub: [Nanogpt-modded](https://github.com/KellerJordan/modded-nanogpt)


Doc listing all changes: [Nanogpt Modded Change Log](https://docs.google.com/document/d/1wOxjaMrLdkhbev2AHD2voz45OMjWCvSKbINwGTmQ19c/edit?usp=sharing)

Architecture details:

* Mixtral-style Mixture of Experts (MoE)
* Top-2 experts chosen
* Noisy Top-K router to avoid expert bias

PRs are welcome.


Checklist of all completed changes: 


- [x] Tuned learning rate & rotary embeddings
- [x] Introduced the Muon optimizer
- [x] Muon improvements
- [x] Pad embeddings, ReLU², zero-init projections, QK-norm
- [x] Distributed the overhead of Muon
- [x] Untied embedding and head
- [x] Value and embedding skip connections, momentum warmup, logit softcap
- [x] Bfloat16 activations
- [x] U-net pattern skip connections & double lr
- [x] 1024-ctx dense causal attention → 64K-ctx FlexAttention ( post this change due to some bug in flex attention for B,S,H values, all of the following scripts have a torch compile bug<<working to solve :)>>) 
- [x] Attention window warmup
- [x] Value Embeddings
- [x] U-net pattern value embeddings, assorted code optimizations
- [x] Split value embeddings, block sliding window, separate block mask
- [x] Sparsify value embeddings, improve rotary embeddings, drop an attn layer
- [x] Lower logit softcap from 30 to 15
- [x] FP8 head, offset logits, lr decay to 0.1 instead of 0.0
- [x] Merged QKV weights, long-short attention, attention scale, lower Adam epsilon, batched Muon
- [x] Reduced batch size
- [ ] Faster gradient all reduce
- [ ] Overlap computation and gradient communication


