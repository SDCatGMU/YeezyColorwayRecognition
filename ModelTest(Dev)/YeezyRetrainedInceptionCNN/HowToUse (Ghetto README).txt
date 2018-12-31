pip install tensorflow

make a directory 

curl -LO https://github.com/tensorflow/hub/raw/master/examples/image_retraining/retrain.py

Obtain folder of catogerized photos called training_data and place in current directory

python retrain.py --image_dir D:\Documents\ML\example_code\training_data

model and label D:\tmp\output_graph.pb and D:\tmp\output_labels.txt

curl -LO https://github.com/tensorflow/tensorflow/raw/master/tensorflow/examples/label_image/label_image.py

Obtain testing image called test.png (or whatever format of image just use the same name below) place in folder testing_data

python label_image.py --graph=/tmp/output_graph.pb --labels=/tmp/output_labels.txt --input_layer=Placeholder --output_layer=final_result --image=./testing_data/test.png(or use full dir path for this)