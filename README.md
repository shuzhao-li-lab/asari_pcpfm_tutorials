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

TODO

## Tutorial Preparation

### Input Data
The tutorial will cover running Asari in the context of the pipeline and standalone. This requires that we have a few datasets to play with. Also you will need several sources of known metabolites for annotation. If you are a non-commercial user, you can easily install these by running:

`pcpfm download_extras`

Which will provide the HMDB, the LMSD, and MoNA for Level 4 and Level 2 annotation respectively. Note that you have to type `yes` in order to download these data sources. 

Now the pipeline is ready but you will need some data to play with. 

These datasets are publically available and will be referred to throughout the tutorial. 

1. HZV029 subset:
2. HZV029: https://www.metabolomicsworkbench.org/data/DRCCMetadata.php?Mode=Study&StudyID=ST002233&StudyType=MS&ResultType=5

###




