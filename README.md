# Denoising Using Autoencoders

Audio denoising with a 1D convolutional autoencoder in PyTorch. A waveform is loaded with `librosa`,
Gaussian noise is added, and the network is trained to reconstruct the clean signal.

| Notebook | Contents |
|---|---|
| `Denoising_using_autoencoder.ipynb` | The main notebook. Loads a clip, normalises each channel, trains the autoencoder with Adam, adds noise (sigma 0.05) and plays back the noisy and reconstructed audio. |
| `Denoise.ipynb` | An earlier variant with an encoder/decoder that also produces a mean and standard deviation of the latent code, trained on short clips and checked on held-out ones. |

## Notes

- Both notebooks were written for **Google Colab** and mount Google Drive (`/content/drive/MyDrive/Test Audio/...`).
  The audio files are **not included**; point the paths at your own clips.
- `Denoise.ipynb` can optionally use a random-direction optimiser from a module called `optimrandomdir_pytorch`,
  which is not in this repository. It is off by default.

## Running

```bash
pip install torch librosa numpy scipy matplotlib
jupyter notebook
```
