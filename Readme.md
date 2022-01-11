# Useful Troubleshooting

### Anaconda FAQ
Try to install as much as possible via anaconda before resorting to below:

#### Compile Pytorch for compatiable with GTX3080
conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch

#### Torchtext
##### Torchtext conda
conda install -c pytorch torchtext 

##### To fix torchtext.data not found
torchtext.data --> torchtext.legacy.data

#### Spacy
conda install -c conda-forge spacy
###### OSError: [E050] Can't find model 'en_core_web_sm'. It doesn't seem to be a shortcut link, a Python package or a valid path to a data directory. · Issue #4577 · explosion/spaCy
conda install -c conda-forge spacy-model-en_core_web_sm 

### To create Jupyter Notebook Env
source activate myenv or conda activate myenv
python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
