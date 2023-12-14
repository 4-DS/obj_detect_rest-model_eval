# Step CV-Pipeline: model_eval

This step CV-Pipeline: model_eval is intended for:
This stage of the CV Pipeline Model_Eval ensures model testing, performance evaluation, saving predictions for further analysis, and visualizing results using metrics and graphs.

Input data for step CV-Pipeline: model_eval
- **coco_test_dataset**     
Test dataset (from the CV-Pipeline component: data_prep)
- **bento_service**     
bento_service, packaged model service via BentoML (from CV-Pipeline component: model_pack)

## How to run a step CV-Pipeline: model_eval

### Create a directory for the project (or use an existing one)
```
mkdir -p obj_detect_rest
cd obj_detect_rest
```

### clone the repository: model_eval
```
git clone --recurse-submodules https://github.com/4-DS/obj_detect_rest-model_eval.git {dir_for_model_eval}
cd {dir_for_model_eval}
```  

### run step CV-Pipeline:model_eval
```
python step.dev.py
```  
or
```
step.prod.py
``` 