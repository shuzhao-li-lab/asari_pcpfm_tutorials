# Setup
## Datasets for testing:

You will need to download two datasets for running these tutorials.

The first is the bowen_2023 dataset: 

https://drive.google.com/file/d/14dYpVU40nIjblraOYKE1jXRxHk4LX66D/view?usp=drive_link

The next is the HZV029 subset dataset:

https://drive.google.com/file/d/1PikUcw3fyF3AgMjCqp42hyVhEvl4Y5mw/view?usp=drive_link

Download to your downloads folder and then unzip it in that directory

## System Preparation
Asari and the pcpfm requires python3 and several python3 libraries. 

### MacOS
For MacOS, python3 comes installed natively. Test that you have Python3 and it works by ›‹›

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/ec571548-7bdf-44b4-ae68-9b4a6aa6eb85)

^^ clicking on the search icon (magnifying glass) and typing "terminal". You should get a dialog like this:

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/0c08dc0a-dc99-4209-bfe5-c8bae8e4b503)

Hit enter and you should now see a terminal window:

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/02f67f74-8cb8-44b0-8792-c999c07e1ba8)

Type `which python3` and you should get back a path. If you do not get anything returned from that command you need to install python3. Here are instructions: https://docs.python-guide.org/starting/install3/osx/

Next you will need to install the pipeline and asari. You can do this with a single command `pip3 install pcpfm`: 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/e9d9dee8-f7b3-4f28-ab77-fc0284fea53d)

If you get an error about "is not on PATH":

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/a1909a6d-b19f-457e-b005-39019d51d4bd)

Here is the fix. You simply need to add the directory mentioned above to $PATH:

`export PATH=<DIRECTORY>:$PATH`, in this example, it is: `export PATH=/Users/mitchjo/Library/Python/3.9/bin/:$PATH`

**Note that this will only work for the current terminal window. If you open or close a window, you will need to rerun this command. **

Now run `pcpfm` in the terminal window, you will get an error but you should see this message: 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/4f5a640c-70fe-4525-bb71-8ac794dc71a5)


### Windows 10

Note, I'm not much of a windows user, so these instructions will need improvement. 

Download and install Python3: https://www.python.org/downloads/, I recommend the most recent under specific releases (currently 3.11.8).

Now you will need to add Python3 to your PATH. You can do this using powershell or windows terminal which you can find in the windows start bar if you search for 'powershell' or 'terminal'.

Now you should be able to install packages via pip from powershell or terminal:

`pip3 install pcpfm` or `pip install pcpfm`

and 

`pip3 install asari-metabolomics` or `pip install asari-metabolomics`

## Tutorial Preparation

### Input Data
The tutorial will cover running Asari in the context of the pipeline and standalone. This requires that we have a few datasets to play with. Also you will need several sources of known metabolites for annotation. If you are a non-commercial user, you can easily install these by running:

`pcpfm download_extras`

Which will provide the HMDB, the LMSD, and MoNA for Level 4 and Level 2 annotation respectively. Note that you have to type `yes` in order to download these data sources. 

Now the pipeline is ready but you will need some data to play with. 

### 

# Tutorials

## Asari.app Tutorial

Asari online is limited to 1 Gb of input files, for this test lets use the **HZV029 subset**. 

In your browser of choice, navigate to `https://asari.app/process`.

The HZV029 dataset is a HILIC positive dataset acquired on an oribtrap. we can safely assume that the mass accuracy is 5 ppm. You will need to provide an email to get a notification when your job is completed:

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/bb5acbfa-1931-4832-85e1-adce7e09d404)

Now navigate to the next page by selecting `save params`. Here you need to drag the 10 mzML files into this window:

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/78c96f55-217d-4cc9-b1e9-d94502038c53)

Then click upload all: 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/019be76a-0c59-4547-8773-ab79923eda98)

After upload you should see this:

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/e32fe1ff-652d-4a12-be33-c1d6ce28ecca)

Now click `process`and you will see something like this: 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/76ee201e-7f83-4db9-bbc3-d3a42e47713a)

Record the TASK ID somewhere, you can use it to retrieve results. Now wait...

After a few minutes you should see this: 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/f520659f-d3b6-4ec6-989b-c871f53b4758)

Now click `get results`, now you will see the result pane. You can check out various statistics. 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/43919a67-f6dd-4032-8454-8666be8fac1b)

The results can be downloaded using `download results`. This will download a .zip file that when opened has a number of files including the preferred feature table and the full feature table under the export subdirectory. 

![image](https://github.com/shuzhao-li-lab/pcpfm_tutorials/assets/10132705/55c7f8b4-50f0-4df6-9a66-a2dc9a7a78fb)

## basic pcpfm usage

follow the HZV029 subset notebook under notebooks

## feature detection and asari viz

follow the bowen_cell notebook under notebooks





