# Introduction

Simple tools that convert files between json/csv.

## csv2json

`usage: csv2json [-h] [-o [OUTPUT]] [--indent [INDENT]] [input]`

Input is given by either stdin or the first argument. The first line of the input should be column names.
Output will be printed through stdout, but `-o` option will redirect it to a file.
There is also `--indent` option. If not given, the default indentation is 2 spaces.

    $ ./csv2json sample.csv
    (jsonified 'sample.csv' will be printed)
    $ ./csv2json sample.csv -o sample.json
    $ ./csv2json < sample.csv > sample.json
    $ ./csv2json sample.csv > sample.json --indent 4

## json2csv

`usage: json2csv [-h] [-o [OUTPUT]] [input]`

Input is given by either stdin or the first argument.
Output will be printed through stdout, but `-o` option will redirect it to a file. The column order of the output will be arbitrary.

    $ ./json2csv sample.json
    (csv version of 'sample.json' will be printed)
    $ ./json2csv sample.json -o sample.csv
    $ ./json2csv < sample.json > sample.csv