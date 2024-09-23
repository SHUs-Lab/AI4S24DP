
# Experiment Instructions

**For all experiments pip install necessary python packages
listed in Libraries**

 ## Single Pretrained Model: 
 *The following shows how to get the benchmarks for static and dynamic model growth techniques.*

 - **Dynamic growth**
	 - To benchmark the Shakespear dataset, use the
file ’LiGO_Shakespear.ipynb’ in the directory ’Dynamic-
ModelGrowth’.
    -  To benchmark the Wiki-2 and Wiki-103 datasets,
use the file ’LiGO_Wiki.ipynb’ in the directory ’Dynamic-
ModelGrowth’. 
    - To choose the dataset, modify block 3 by
toggle commenting lines 2 and 5.
 - **Static Growth**

    - To benchmark the Shakespear dataset, run the
file ’WideAndDeep_Shakespear.ipynb’ in directory ’Static-
ModelGrowth’.
    -  To benchmark the Wiki-2 and Wiki-103 datasets,
run the file ’WideAndDeep_Wiki.ipynb’ in directory ’Static-
ModelGrowth’.
    -  To choose the dataset, modify block 3 by
toggle commenting lines 2 and 5.
## Multi-Model: 
*Do the following steps for Multi-Model evaluation*

 - Files are located in Multi-Model folder 
 - Choose dataset with the associated load_dataset() function call in both ’LiGO-MultiModel.ipynb’ and ’Stacked-MultiModel.ipynb’ 
 - Run the Scripts ’LiGO-MultiModel.ipynb’ and ’Stacked- MultiModel.ipynb’ to generate performance results for multi-model techniques

### Calculating FLOPS: 
To calculate the FLOPs associated with a particular model dimension run the following code at the end of any of the scripts.

  

    sample = None
	for i in train_dataloader:
	    sample = i['input_ids']
	    break
    calculate_flops(model=Model(model_dim).to(device), kwargs={'inp':sample})

### Datasets

 - Shakespeare: Downloaded from 
   [here](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)
  - Wikitext-2: Downloaded from huggingface https://huggingface.co/datasets/Salesforce/wikitext 
  - Wikitext-103: Downloaded from huggingface https://huggingface.co/datasets/Salesforce/wikitext
