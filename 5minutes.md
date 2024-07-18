# Asari in 5 minutes


[in work]


## Asari on command line

If installed from pip, one can run `asari` as a command in a terminal, followed by a subcommand for specific tasks.

For help information:

`asari -h`

To process all mzML files under directory mydir/projectx_dir:

`asari process --mode pos --input mydir/projectx_dir`

To get statistical description on a single file (useful to understand data and parameters):

`asari analyze --input mydir/projectx_dir/file_to_analyze.mzML`

To launch a dashboard in your web browser after the project is processed into directory process_result_dir:

`asari viz --input process_result_dir`

Alternative to a standalone command, to run as a module via Python interpreter, one needs to point to module location, e.g.:

`python3 -m asari.main process --mode pos --input mydir/projectx_dir`



## feature detection and asari viz

follow the bowen_cell notebook under notebooks

