# flask/gunicorn based Heroku web app for brain tumour detection

[![](https://img.shields.io/badge/python-2.7%2C%203.5%2B-green.svg)]()



------------------
## About the app
> This repository was created to help clarify how to utilise flask and gunicorn to easily deploy a python/keras deep learning model as a web app on Heroku. This example features code for online deployment of a multi-class medical image classification model, based on ResNet-50 network architecture.  The trained model achieved accuracy of more than 98.8% on the test set and its weights have been saved in the Models folder  in the very useful HDF5 format. As we cannot keep the file on github > 25 MB you can download the resnet50 model using this [link](https://drive.google.com/file/d/1l2rfpPdruJHSl8w6DpQj-eJ8Za6cr2ju/view?usp=sharing) You may use your own saved trained model! Just make sure you put it in the Models folder and name it appropriately so that the flask app may call it.

> A JavaScript app running on the browser calls the Flask app (app.py) to load the model weights and return results to the JavaScript  app (through the 'GET' and 'POST' methods).



> This web application has been created and the changes to whatManu Siddhartha  had already prepared were the following:
<ul>
<li>Inclusion of a procfile to serve the app with gunicorn on the Heroku server after upload (for uploading this python app to Heroku please follow Heroku documentation on how to use git with Heroku)</li>
<li>As per Heroku requirements for stability and reproducibility, versions of all required python environments were specified in the requirements.txt file</li>
<li>Inclusion of gunicorn to the requirements.txt file</li>
<li>Changed the app.py (flask app) file to adapt it to the required functionality according to the trained binary image classification model. The program was also modified to delete every uploaded image after providing the prediction. This will prevent exceeding capacity limits on Heroku servers. The last lines of the file have been modified to work with gunicorn. </li>
<li>The Index.html and base.html files have been modified accordingly to include references and information about the model</li>
<li>This README file has been adapted to provide instructions about heroku deployment. The part for customisation has been modified also</li>
</ul>

> To create a web app that runs locally follow instructions in the README file, to run the model locally. Gevent or gunicorn may be used for local deployment too.

## Customization options

### Use your own model

Place your trained keras deep learning model to the models directory.


### Use other pre-trained model

See [Keras applications](https://keras.io/applications/) for more available models such as DenseNet, MobilNet, NASNet, etc.


### UI Modification

Modify files in `templates` and `static` directory.

`index.html`, `base.html` for the UI and `main.js` for all the behaviors

## Deployment

To deploy it for public use, you need to upload this app on heroku or other python enabled server. However heroku is pretty good at recognising and running python apps. There is also a free version!

## More resources

Check Siraj's ["How to Deploy a Keras Model to Production"](https://youtu.be/f6Bf3gl4hWY) video. The corresponding [repo](https://github.com/llSourcell/how_to_deploy_a_keras_model_to_production).

[Building a simple Keras + deep learning REST API](https://blog.keras.io/building-a-simple-keras-deep-learning-rest-api.html).

[How to deploy a Flask App to Heroku](https://progblog.io/How-to-deploy-a-Flask-App-to-Heroku/).

"# deep-learning-brain-tumour-detection" 
"# brain-tumour-detection-web-app" 
