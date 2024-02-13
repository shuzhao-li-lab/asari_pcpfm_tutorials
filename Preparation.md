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

### Windows 10

TODO

## Tutorial Preparation

The tutorial will cover running Asari in the context of the pipeline and standalone. This requires that we have a few datasets to play with. 


