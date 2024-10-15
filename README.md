## Environment

```
conda create -n pi python==3.9
conda activate pi
pip install transformers==4.10.0
pip install pytorch-lightning==1.5.1
pip install pandas rouge scipy
Pip install numpy==1.23.0
# if you want to re-produce our data preparation process
pip install scikit-learn plotly
```
# Download data

You can download the models we trained  from [Here](https://pan.baidu.com/s/1JQQtKOKY3bK1a4pyjZOIHg?pwd=3s33 "title")

# Training
 python train.py --gpus 8 --batch_size 8 --arch base --setup transformer

 # Evaluation

1.The simplest command below can show you results of automatic metrics (Bleu, METEOR, and ROUGE)

  python translate.py $path_to_model
  
2.save the generated patient instructions by running:

  python translate.py $path_to_model --save_json --save_base_path ./inference_results --save_folder "" --json_file_name preds_and_scores.json 
