# Developing in a Non-Anaconda Virtual Environment"

Lots of developers use Anaconda. It is your choice to use Anaconda or not.
`virtualenv` is also a famous tool for python developers and has `pip` supports.

## What is a Virtual Environment?
Its name looks like it is very complex concept, but it is not. 
Virtual Environment is a tool to keep the dependencies and libraries required by different projects in a separate space. 
So usually you set up a virtual environment for specific projects that needs special dependencies.  
For Example, when i was using Tensorflow 2.0 beta version, since 2.0 beta did not support python 3.6, I had to set up a
virtual environment that has TF 2.0, python 3.6 and all the other dependencies inside. 
(Now Tensorflow 2.0 stable version has released, and they support python 3.7 as well).  
So how do you do this?

## Creating Virtual Environment
**1. let's check if you have recent version of python installed.**  
On your terminal type:
```
$ python3 --version
```
It should be 3.4 or later.  


**2. install virtualenv tool via pip3** 
```
$ sudo pip3 install -U virtualenv
```

**3. create your own virtual environment.**  
```
$ virtualenv -p python3.8 comp0189
```


**4. know how to turn on and off our virtual environment**  
To initiate:
```
$ source comp0189/bin/activate
```

To deactivate:
```
$ deactivate
```

**5. install everything you need in the Environment**  
Access to your environment and do things you need:
```
(comp0189) $ pip install --upgrade pip
(comp0189) $ pip install numpy==1.19.1
```