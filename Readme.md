# Useful Troubleshooting

## Anaconda FAQ
Try to install as much as possible via anaconda before resorting to below:
General Rule of thumb: If Module cannot be found. Try to install via conda command, last resort is to use pip

### Compile Pytorch for compatiable with GTX3080
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch
### Torch.cuda.is_available() returns False, nvidia-smi is working
Remove pytorch and install again via the above command

### Torchtext
##### Torchtext conda
conda install -c pytorch torchtext 

##### To fix torchtext.data not found
torchtext.data --> torchtext.legacy.data

### Spacy
conda install -c conda-forge spacy
###### OSError: [E050] Can't find model 'en_core_web_sm'. It doesn't seem to be a shortcut link, a Python package or a valid path to a data directory. · Issue #4577 · explosion/spaCy
conda install -c conda-forge spacy-model-en_core_web_sm 

### Jupyter
##### To create Jupyter Notebook Env
source activate myenv or conda activate myenv
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
Preferred Choice: Use Visual Studio Code for Jupyter

##### IProgress not found.
Use Anaconda to install ipywidgets

### Rstudio on Ubuntu via Conda
Create new env for Rstudio, Rstudio cannot be installed in the base environment. Preferred solution is to create install Rstudio as independent application
