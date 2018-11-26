## Real-time Object Detection on Movidius  
### Flow  
1.Export your model's graphdef (you can use tf.train.write_graph to export the graphdef from within your tf session)  
2.Freeze your graphdef using freeze_graph.py (you'll need the checkpoint files)  
3.Pass the frozen model to mvNCCompile along with the input and output nodes.  
### Caffe  
```
mvNCCompile network.prototxt [-w network.caffemodel] [-s max_number_of_shaves] [-in input_node_name] [-on output_node_name] [-is input_width input_height] [-o output_graph_filename] [-ec]
```
### Tensorflow  
```
mvNCCompile network.meta [-s max_number_of_shaves] [-in input_node_name] [-on output_node_name] [-is input_width input_height] [-o output_graph_filename] [-ec]
```