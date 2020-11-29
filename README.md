# HANDWRITTEN-DIGIT-RECOGNITION



## Table of Content
  * [Overview](#overview)
  * [Motivation](#motivation)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Run](#run)
  * [Deployement on Heroku](#deployement-on-heroku)
  * [Directory Tree](#directory-tree)
  * [To Do](#to-do)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technologies Used](#technologies-used)
  * [Team](#team)
  * [License](#license)
  * [Credits](#credits)


## Overview
Handwritten Digit Recognition using OpenCV, sklearn and Python

## Motivation
What could be a perfect way to utilize unfortunate lockdown period? Like most of you, I spend my time in cooking, Netflix, coding and reading some latest research papers on weekends. The idea of classifying indian currency struck to me when I was browsing through some research papers. I couldn't find any relevant research paper (and of course dataset!) associated with it. And that led me to collect the images of Indian currency to train a deep learning model using [this](https://github.com/hardikvasa/google-images-download) amazing tool.
## Technical Aspect
This repository contains the following files-

1. `generateClassifier.py` - Python Script to create the classifier file `digits_cls.pkl`.
2. `performRecognition.py` - Python Script to test the classifier.

```python
python generateClassifier.py
```
* To test the classifier, run the `performRecognition.py` script.
```python
python performRecognition.py -c <path to classifier file> -i <path to test image>
```
ex -
```python
python performRecognition.py -c digits_cls.pkl -i photo_1.jpg
```

## Installation
The Code is written in Anaconda 3.7. If you don't have Python installed you can find it [here](https://www.conda.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
conda install -r requirements.txt


## Run
> STEP 1
#### Linux and macOS User
Open `.bashrc` or `.zshrc` file and add the following credentials:
```bash
export AWS_ACCESS_KEY="your_aws_access_key"
export AWS_SECRET_KEY="your_aws_secret_key"
export ICP_BUCKET='your_aws_bucket_name'
export ICP_BUCKET_REGION='bucket_region'
export ICP_UPLOAD_DIR='bucket_path_to_save_images'
export ICP_PRED_DIR='bucket_path_to_save_predictions'
export ICP_FLASK_SECRET_KEY='anything_random_but_unique'
export SENTRY_INIT='URL_given_by_sentry'
```
Note: __SENTRY_INIT__ is optional, only if you want to catch exceptions in the app, else comment/remove the dependencies and code associated with sentry in `app/main.py`

#### Windows User
Since, I don't have a system with Windows OS, here I collected some helpful resource on adding User Environment Variables in Windows.

__Attention__: Please perform the steps given in these tutorials at your own risk. Please don't mess up with the System Variables. It can potentially damage your PC. __You should know what you're doing__. 
- https://www.tenforums.com/tutorials/121855-edit-user-system-environment-variables-windows.html
- https://www.onmsft.com/how-to/how-to-set-an-environment-variable-in-windows-10


## Directory Tree 
```
├── app 
│   ├── __init__.py
│   ├── main.py
│   ├── model
│   ├── static
│   └── templates
├── config
│   ├── __init__.py
├── processing
│   ├── __init__.py
├── requirements.txt
├── runtime.txt
├── LICENSE
├── Procfile
├── README.md
└── wsgi.py
```

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://keras.io/img/logo.png" width=200>](https://keras.io/) [<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/streamlit-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://www.kindpng.com/picc/b/301/3012484.png" width=200>](https://aws.amazon.com/s3/) 

[<img target="_blank" src="https://sentry-brand.storage.googleapis.com/sentry-logo-black.png" width=270>](https://www.sentry.io/) [<img target="_blank" src="https://openjsf.org/wp-content/uploads/sites/84/2019/10/jquery-logo-vertical_large_square.png" width=100>](https://jquery.com/)

## License
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits
- [Google Images Download](google-images-download) - This project wouldn't have been possible without this tool. It saved my enormous amount of time while collecting the data. A huge shout-out to its creator .


