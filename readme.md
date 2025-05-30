Sure, here's your README written in clean Markdown, preserving your style and with all links properly formatted:

---

````
Please run `data.py` in the `trainers` folder first in the same directory where the training code lives.

Sample usage:
```bash
python train_muon.py --experiment_name muon
````

For logging:

```bash
python logger.py --experiment_name muon
```

Sample for profiling:

```bash
python train_muon.py --experiment_name muon --enable_profiling
```

# About

This repo is an attempt to port all changes of nanogpt modded by Keller Jordan
GitHub: [Nanogpt-modded](https://github.com/KellerJordan/modded-nanogpt)
Doc listing all changes: [Nanogpt Modded Change Log](https://docs.google.com/document/d/1wOxjaMrLdkhbev2AHD2voz45OMjWCvSKbINwGTmQ19c/edit?usp=sharing)

Architecture details:

* Mixtral-style Mixture of Experts (MoE)
* Top-2 experts chosen
* Noisy Top-K router to avoid expert bias

PRs are welcome.

```

Let me know if you want to append the checklist or license section.
```
