To set up the environment, please use:

```
module load python
conda create -n test-exclusive python=3.6 -c conda-forge --yes
source activate test-exclusive
conda install -c conda-forge numpy cython dask matplotlib multiprocess numdifftools scikit-learn scipy ipykernel --yes

git clone https://github.com/HerculesJack/bayesfast
cd bayesfast
git checkout dev
pip install -e .

python -m ipykernel install --user --name test-exclusive --display-name test-exclusive
```


The two notebooks, `shared.ipynb` and `exclusive.ipynb`, have the same content,
but were running on `cori-shared-node-cpu` and `cori-exclusive-node-cpu`, respectively.
