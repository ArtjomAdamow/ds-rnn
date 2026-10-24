# Recurrent Neural Networks and Transformers

Two hands-on notebooks on the architectures built for sequential data. The first covers recurrent networks, why their gradients vanish over long sequences, and how LSTM and GRU gating addresses it. The second builds a Transformer encoder from scratch, starting with scaled dot-product attention and ending with a working sequence classifier.

## Learning Objectives

By the end of this repository, you should be able to:

- Build and train SimpleRNN, LSTM and GRU models in TensorFlow/Keras.
- Measure how a gradient shrinks or grows as it travels back through time, and explain what gating changes.
- Implement scaled dot-product attention, multi-head attention and positional encoding from scratch.
- Assemble a Transformer encoder from attention, feed-forward blocks, residual connections and layer normalisation.
- Compare recurrent and attention-based models on parameter cost and on how each one processes a sequence.
- Apply an LSTM to a time series forecast and evaluate it against a baseline using MAE and RMSE.

## Learning Path

Work through the notebooks in this order:

| File / Folder                                              | Description                                                                                               |
| ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [**Recurrent Neural Networks**](1_rnn_intro.ipynb)         | RNNs on sequential data, the vanishing gradient problem measured directly, LSTM and GRU gating, and a time series forecast. |
| [**Transformers and Attention**](2_transformer_intro.ipynb) | Attention from first principles, multi-head attention, positional encoding, and a full encoder used for classification. |

### Additional Folders and Files

| File / Folder                        | Description                                     |
| ------------------------------------ | ----------------------------------------------- |
| [**Solutions**](solutions/)          | Reference solutions for the exercise sections.  |
| [**pyproject.toml**](pyproject.toml) | Project configuration and dependencies.         |
| [**uv.lock**](uv.lock)               | Dependency lock file.                           |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it including the `< >` brackets with your own value. For example, `cd <repo-name>` becomes `cd ds-rnn-transformers`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

This installs all dependencies and creates a virtual environment in `.venv/`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the environment created by `uv sync`.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the Python environment created by `uv sync` as the kernel.

> [!TIP]
> The notebooks train small models on synthetic data, so everything runs on a CPU in a few minutes. No GPU is required.

## References & Further Reading

- [**Understanding LSTM Networks**](https://colah.github.io/posts/2015-08-Understanding-LSTMs/): Christopher Olah's walkthrough of the LSTM cell, with the clearest diagrams of the gates.
- [**The Unreasonable Effectiveness of Recurrent Neural Networks**](https://karpathy.github.io/2015/05/21/rnn-effectiveness/): Andrej Karpathy trains character-level RNNs on real text and inspects what they learn.
- [**On the difficulty of training Recurrent Neural Networks**](https://arxiv.org/abs/1211.5063): Pascanu, Mikolov and Bengio on vanishing and exploding gradients.
- [**Attention Is All You Need**](https://arxiv.org/abs/1706.03762): the original Transformer paper, whose Section 3 maps onto the second notebook.
- [**The Illustrated Transformer**](https://jalammar.github.io/illustrated-transformer/): Jay Alammar's visual introduction to attention and the encoder stack.
- [**Working with RNNs**](https://www.tensorflow.org/guide/keras/working_with_rnns): the TensorFlow guide to recurrent layers.
- [**Jupyter Notebooks in VS Code**](https://code.visualstudio.com/docs/datascience/jupyter-notebooks): how to run and debug notebooks in the editor.
