# Asari in 5 minutes

Asari is a software tool for metabolomics data preprocessing. It's designed from ground up for new data models, algorithms and implementation. As a result, tools are reusable and chainable, and performant (Nature Communications, 14(1), p.4113; Analytical chemistry, 95(15), pp.6212; PLOS Computational Biology, 20(6), p.e1011912).

## Input files are centroid mzML files 
We use ThermoRawFileParser (https://github.com/compomics/ThermoRawFileParser) to convert Thermo .RAW files to .mzML. 
Msconvert in ProteoWizard (https://proteowizard.sourceforge.io/tools.shtml) can handle the conversion of most vendor data formats and .mzXML files.

Our [MT02 dataset](https://github.com/shuzhao-li-lab/data/raw/main/data/MT02Dataset.zip) can be used for testing.

## If you don't want to deal with command line -
You can use the asari web app at https://asari.app/ ([tutorial for the web app](/webapp.md)). 

Its free quota is currently limited to 1 Gb of input files. The app generates a set of output files you can download.

## You will be a power user by using the command line -
Suppose you have Python 3.8 or higher. Install asari by 
 `pip3 install asari-metabolomics`. Add `--upgrade` to update to new versions.

If you need Python and other tools, please refer to [this page](/Installation_Preparation.md).

If installed from pip, one can run `asari` as a command in a terminal, followed by a subcommand for specific tasks.
To process all mzML files under directory mydir/projectx_dir:

`asari process -i mydir/projectx_dir`

Alternative to a standalone command, to run as a module via Python interpreter, one needs to point to module location, e.g.:

`python3 -m asari.main process --mode pos --input mydir/projectx_dir`

## Output

A typical run on disk may generatae a directory like this

    rsvstudy_asari_project_427105156
    ├── Annotated_empricalCompounds.json
    ├── Feature_annotation.tsv
    ├── export
    │   ├── _mass_grid_mapping.csv
    │   ├── cmap.pickle
    │   ├── full_Feature_table.tsv
    │   └── unique_compound__Feature_table.tsv
    ├── pickle
    │   ├── Blank_20210803_003.pickle
    │   ├── ...
    ├── preferred_Feature_table.tsv
    └── project.json

The recommended feature table is `preferred_Feature_table.tsv`. 

All peaks are kept in `export/full_Feature_table.tsv` if they meet signal (snr) and shape standards.  

## Visualization Dashboard
After data are processed, users can use 

`asari viz --input process_result_dir` 

to launch a dashboard to inspect data, where 'process_result_dir' refers to the result folder. 
 
![viz_screen_shot](https://github.com/shuzhao-li-lab/asari/blob/main/docs/source/_static/viz_screen_shot20220518.png)

## What about parameters?
One can call `asari -h` to see commands and arguments.
Default m/z precision is set at 5 ppm. Default ionization mode is `pos`. Change to `neg` if needed, by specifying `--mode neg` in command line.
Most people need not bother with other parameters.

## More 
- Asari source code: https://github.com/shuzhao-li/asari. 
- More utorials are at:  https://github.com/shuzhao-li-lab/asari_pcpfm_tutorials.
