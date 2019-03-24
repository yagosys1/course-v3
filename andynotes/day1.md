#1 Jupyiter tutorials

https://www.cheatography.com/weidadeyue/cheat-sheets/jupyter-notebook/pdf_bw/
Esc 
a/b 
dd

#2 about fastai datasets

URLs.PETS  are imported from fastai.vision 
the destination of data is stored under the location specified in ~/.fastai/config.yml
➜  .fastai cat config.yml
data_path: /Users/interbeing/.fastai/data
model_path: /Users/interbeing/.fastai/models
➜  .fastai pwd
/Users/interbeing/.fastai

# regex

a='/home/ubuntu/.fastai/data/oxford-iiit-pet/images/newfoundland_95.jpg'

pat = r'/([^/]+)_\d+.jpg$'

r1 = re.findall(pat,a)

r1=newfoundland

pat= r'/([^/]+)_\d+.jpg$'

r == mean this is regress expression

'/xxxxjpg$'  mean a string start with '/' and end with 'jpg'

() capture groud, anything captured here will assigned to variable r1
[^/] means in the group which  is not '/' 
+ means [^/] at least 1 or more times
_ means string '_'
\d+ means digital at least 1 or more.
.jpg means string '.jpg'

what we want to capture is a string that start with '/' and end with string plus digitial at the end, but we only take the string part which is inside the capture group (). 
 
# download data set with curl
curl -O -C - https://s3.amazonaws.com/fast-ai-imageclas/oxford-iiit-pet.tgz

'-C - ' means resume if interupted 
or 
wget -c https://s3.amazonaws.com/fast-ai-imageclas/oxford-iiit-pet.tgz

#pathlib (this is new in 3.4 version)


path_anno = path/'annotations'  

this is same os 
os.path.join(os.getcwd(), "annotations")
or 
os.path.join('/Users/interbeing/.fastai/data/oxford-iiit-pet',"annotations")

# display where the model is saved
learn.save('stage-1',return_path=True)

force to disable cuda

```
CUDA_VISIBLE_DEVICE=''
or
fastai.torch_core.defaults.device='cpu'

