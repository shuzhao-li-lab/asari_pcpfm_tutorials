# How to install the software and get example data

If you know this piece of code:
`pip install pcpfm`, you are good to go. 

> **Explanation:** Asari and pcpfm depend on Python3 and some libraries. By install pcpfm using the pip tool, the dependency libraries will be installed as well. Replace pcpfm with asari-metabolomics if you are not ready to install the full pipeline.

For others, we recommend to install one of the these options:
- [VS Code](https://code.visualstudio.com/download). Then install Python and Jupyter notebook within VS Code.
- [Anaconda](https://docs.anaconda.com/anaconda/install/). Within Anaconda Navigator, you can find the notebook.

> **Explanation:** What you really need is Python3 and some libraries on your computer. Their installation involves details for different operating systems. The above tools take care of most these details for you. VS Code is a development environment; Anaconda is a scientific computing environment. We want Jupyter Notebook to illustrate what the code does. 

The software should be ready now.

> **Note:** If you run into any installation problems, you have a better chance to solve them by calling your computer friends. These are usually not specific to our software.

## Datasets we use for tutorials:

MT02 dataset:
https://github.com/shuzhao-li-lab/data/raw/main/data/MT02Dataset.zip

**Optional**
- Bowen_2023 dataset:
https://drive.google.com/file/d/1EUldDALjPYmmjZrAez4l26RVnDVDtCNF/view?usp=sharing

- HZV029 subset:
https://drive.google.com/file/d/1A9F0MVIX6VMXYH2tKF8krSLuH1aaiMDS/view?usp=drive_link

Download to your downloads folder and then unzip it in that directory.

## We are done now. If and only if you insist on doing your own things...

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

Note, I'm not much of a windows user, so these instructions will need improvement. [JM] 

Download and install Python3: https://www.python.org/downloads/, I recommend the most recent under specific releases (currently 3.11.8).

Now you will need to add Python3 to your PATH. You can do this using powershell or windows terminal which you can find in the windows start bar if you search for 'powershell' or 'terminal'.

Now you should be able to install packages via pip from powershell or terminal:

`pip3 install pcpfm` or `pip install pcpfm`

and 

`pip3 install asari-metabolomics` or `pip install asari-metabolomics`
