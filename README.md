<a href="https://arxiv.org/abs/2402.18124">
  <img src="https://img.shields.io/badge/arXiv-2402.18124-b31b1b.svg" alt="arXiv:2402.18124">
</a>

## Dark energy reconstruction analysis with artificial neural networks: Application on simulated Supernova Ia data from Rubin Observatory

This repository contains the code and data used in our paper https://doi.org/10.1016/j.dark.2024.101706. This work presents a model-independent neural network reconstruction of dark energy consistent with theoretical models and real data observations, we use Supernova Ia (SNIa) distance moduli $$\mu(z)$$ and their corresponding statistical errors from three years of simulated SNIa data from the LSST. We incorporate advanced techniques like neural networks, Monte Carlo dropout for uncertainty quantification, and tuning hyperparameters through genetic algorithms using the Tensorflow and DEAP libraries with our [`nnogada` framework](https://github.com/igomezv/Nnogada) for efficient and effective tuning of neural network hyperparameters.


### Repository Structure

- **Data_SNIa_LSST/**: LSST simulated SNIa data used in our analysis.
- **Figures/**: Figures generated from our analysis.
- **chains_mcmc/**: MCMC chains for Bayesian analysis.
- **chains_cov/**: Covariance chains for error estimation.
- **models/**: Trained ANN models.
- **exploratory_test.ipynb**: Notebook for initial data exploration.
- **load_model.ipynb**: Notebook for loading and testing large ANN models.
- **train_model.ipynb**: Main notebook for neural reconstruction of SNeIa.
- **tunning_neural_model.ipynb**: Hyperparameter tuning of the neural model using [`nnogada`](https://github.com/igomezv/nnogada).
- **bayesian_lsst.ipynb**: Notebook for Bayesian analysis of LSST data.


### Usage

- We recommend using an anaconda environment with Python 3.8:
  - `conda create -n neuralsst python=3.8`.
  - `conda activate neuralsst`.

- Then install:
  - `conda install numpy matplotlib pandas scikit-learn seaborn fgivenx tensorflow`
  - `pip install getdist fgivenx astroNN`.

- Finally, if you want to retrain the neural network models with genetic algorithms, please clone or download `nnogada` from [here](https://github.com/igomezv/Nnogada).
  
### Data References
  -Ayan Mitra, Richard Kessler, Surhud More, Renee Hlozek, LSST Dark Energy Science Collaboration, et al. Using host galaxy photometric redshifts to improve cosmological constraints with type ia supernovae in the lsst era. The Astrophysical Journal, 944(2):212, 2023.


### Contributing

We welcome contributions from the community. If you'd like to improve the models, suggest new features, or report issues, please feel free to open an issue or submit a pull request.


### Citing Our Work

If you use the data or methodologies from this repository in your research, please cite our work.

- This paper:
```bibtex
@article{DEreconstructionANN2024,
  title={Dark energy reconstruction analysis with artificial neural networks: Application on simulated Supernova Ia data from Rubin Observatory},
  author={Mitra, Ayan and Gomez-Vargas, Isidro and Zarikas, Vasilios},
  journal={Physics of the Dark Universe},
  volume = {46},
  pages = {101706},
  year = {2024},
  issn = {2212-6864},
  doi = {https://doi.org/10.1016/j.dark.2024.101706},
}
```

- LSST simulations:
```bibtex
@article{mitra2023using,
  title={Using Host Galaxy Photometric Redshifts to Improve Cosmological Constraints with Type Ia Supernovae in the LSST Era},
  author={Mitra, Ayan and Kessler, Richard and More, Surhud and Hlozek, Renee and LSST Dark Energy Science Collaboration and others},
  journal={The Astrophysical Journal},
  volume={944},
  number={2},
  pages={212},
  year={2023},
  publisher={IOP Publishing}
}
```

- Hyperparameter tuning of neural networks with `nnogada`:
```bibtex
@article{nnogada,
  title={Neural networks optimized by genetic algorithms in cosmology},
  author={Gómez-Vargas, I. and Andrade, J. B. and Vázquez, J. A.},
  journal={Physical Review D},
  volume={107},
  number={4},
  pages={043509},
  year={2023},
  publisher={American Physical Society},
  doi={https://doi.org/10.1103/PhysRevD.107.043509},
  url={https://doi.org/10.48550/arXiv.2209.02685}
}
```

- Method for reconstructions with neural networks:
```bibtex
@article{gomez2023neural,
  title={Neural network reconstructions for the Hubble parameter, growth rate and distance modulus},
  author={G{\'o}mez-Vargas, Isidro and Medel-Esquivel, Ricardo and Garc{\'\i}a-Salcedo, Ricardo and V{\'a}zquez, J Alberto},
  journal={The European Physical Journal C},
  volume={83},
  number={4},
  pages={304},
  year={2023},
  publisher={Springer}
}
```
