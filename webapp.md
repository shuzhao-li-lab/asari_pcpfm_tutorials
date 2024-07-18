# Asari.app - the interactive web app for metabolomics data processing

The asari tools are designed for portability. They are first developed as software libraries, then built into various applications. This means the libraries have most functions; a subset is connected to command lines and a smaller subset is connected to the web app. Because the web app depends on how much we can wire into a user-friendly interface within a timeframe.

The URL of asari web app is `https://asari.app/`. 
Its free quota is currently limited to 1 Gb of input files.

The input data should be centroid `.mzML` files. We use ThermoRawFileParser (https://github.com/compomics/ThermoRawFileParser) to convert Thermo .RAW files to .mzML. Msconvert in ProteoWizard (https://proteowizard.sourceforge.io/tools.shtml) can handle the conversion of most vendor data formats and .mzXML files.

We can use the **HZV029 subset** for this tutorial. The HZV029 dataset was acquired on an Oribtrap mass spectrometer coupled with a HILIC LC column using positive ionization (Dr. Maheswor Thapa, Shuzhao Li lab) . we can safely assume that the mass accuracy is 5 ppm. You will need to provide an email to get a notification when your job is completed:

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
