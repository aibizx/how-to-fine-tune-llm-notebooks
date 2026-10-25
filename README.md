# How to Fine-tune Your LLM — notebooks

Runnable companions to **How to Fine-tune Your ~~Dragon~~ LLM**, one of the
[AI/Biz books](https://www.ai.biz/books/fine-tune-llm/).

Every notebook opens directly in Google Colab. Nothing to install.

| Ch | Notebook | Chapter | Open |
|---|---|---|---|
| 1 | `01-when-fine-tuning-is-wrong.ipynb` | [When Fine-Tuning Is the Wrong Answer](https://www.ai.biz/books/fine-tune-llm/when-fine-tuning-is-the-wrong-answer/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/01-when-fine-tuning-is-wrong.ipynb) |
| 2 | `02-prompting-retrieval-fine-tuning.ipynb` | [Prompting, Retrieval and Fine-Tuning](https://www.ai.biz/books/fine-tune-llm/prompting-vs-rag-vs-fine-tuning/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/02-prompting-retrieval-fine-tuning.ipynb) |
| 3 | `03-the-model-enough-to-debug.ipynb` | [The Model, Enough to Debug a Fine-Tune](https://www.ai.biz/books/fine-tune-llm/the-model-enough-to-debug-a-fine-tune/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/03-the-model-enough-to-debug.ipynb) |
| 4 | `04-building-the-dataset.ipynb` | [Building the Dataset](https://www.ai.biz/books/fine-tune-llm/building-the-dataset/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/04-building-the-dataset.ipynb) |
| 5 | `05-instruction-tuning-and-chat-templates.ipynb` | [Instruction Tuning and Chat Templates](https://www.ai.biz/books/fine-tune-llm/instruction-tuning-and-chat-templates/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/05-instruction-tuning-and-chat-templates.ipynb) |
| 6 | `06-lora-and-qlora.ipynb` | [LoRA and QLoRA Explained](https://www.ai.biz/books/fine-tune-llm/lora-and-qlora-explained/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/06-lora-and-qlora.ipynb) |
| 7 | `07-running-the-training-job.ipynb` | [Running the Training Job](https://www.ai.biz/books/fine-tune-llm/running-the-training-job/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/07-running-the-training-job.ipynb) |
| 8 | `08-preference-tuning.ipynb` | [Preference Tuning](https://www.ai.biz/books/fine-tune-llm/preference-tuning/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/08-preference-tuning.ipynb) |
| 9 | `09-evaluating-a-fine-tune.ipynb` | [Evaluating a Fine-Tune Honestly](https://www.ai.biz/books/fine-tune-llm/evaluating-a-fine-tune-honestly/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/09-evaluating-a-fine-tune.ipynb) |
| 10 | `10-quantisation-and-serving.ipynb` | [Quantisation and Serving](https://www.ai.biz/books/fine-tune-llm/quantisation-and-serving/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/10-quantisation-and-serving.ipynb) |
| 11 | `11-a-complete-worked-example.ipynb` | [A Complete Worked Example](https://www.ai.biz/books/fine-tune-llm/a-complete-worked-example/) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aibizx/how-to-fine-tune-llm-notebooks/blob/main/11-a-complete-worked-example.ipynb) |

## Saving your work

Colab opens these notebooks straight from GitHub, so you can run and edit them
immediately. Your changes are **not** saved back on their own. There are two
ways to keep them.

**Save to your Google Drive.** In Colab, choose *File → Save a copy in Drive*.
You get your own copy in your own account, and the original stays as it was.
This is the quickest option if you are just working through a chapter.

**Fork this repository first.** Fork it to your GitHub account, open the
notebook from your fork, and *File → Save a copy in GitHub* will write your
changes back to it. Better if you want your work version controlled, or if you
are going through the whole book.

## Running locally instead

Colab is the fastest way to start, not the only way. Clone or fork this
repository and run everything on your own machine:

```bash
git clone https://github.com/aibizx/how-to-fine-tune-llm-notebooks.git
cd how-to-fine-tune-llm-notebooks

# with uv (fastest)
uv venv && source .venv/bin/activate
uv pip install -r requirements.txt

# or with the standard library
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

jupyter lab
```

On Windows, activate with `.venv\Scripts\activate` instead.

Everything here runs on CPU in PyTorch. Each notebook trains the training
book's small character-level model on *Alice's Adventures in Wonderland* in
about half a minute and fine-tunes that, so no model is downloaded and no
GPU is needed. The longest notebooks take about five minutes.

## How this repo is maintained

Notebooks are authored alongside the chapters in the site repository and pushed
here through the GitHub Contents API. The Colab badge at the top of each
notebook is regenerated on every push, so the links never go stale. Every code
cell is executed before anything is pushed.

Each book gets its own notebook repository, so you can clone just the one you
are working through.

---

MIT licensed. © Sameer Gupta · [ai.biz](https://www.ai.biz/)
