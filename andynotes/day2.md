use colab
https://colab.research.google.com/notebooks/welcome.ipynb#recent=true

make sure elect use gpu. 
runtime--change-runtime-type 

select allow private repro to use your own repo 

use google drive as your data disk

```
from google.colab import drive
drive.mount('/content/gdrive', force_remount=True)
root_dir = "/content/gdrive/My Drive/"
base_dir = root_dir + 'fastai-v3/'
```
ref
https://forums.fast.ai/t/fast-ai-v3-2019/39325/2

gpus on gce are not available at al regions. check
https://cloud.google.com/compute/docs/gpus/


