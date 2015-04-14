# multibatch_jpredapi.pl

This Git repository contains a script which can be used to run many JPred predictions with just one command.


## Requirements:

* Working JPred REST API on the system

You can get it from the official [JPred website](http://www.compbio.dundee.ac.uk/jpred4/api.shtml)

# HOW TO

First you need a list of UniProt accession numbers in a file. One per line. Example (./example_accnums.txt):

    P09867
    P63323
    Q923U9

Then you need fasta files of the above accession numbers in one folder (./example\_fasta\_files/).

Next you can choose which files from the prediction you want to download. Concatenate all file type ending you want to download separated by a colon ':'. The default is to download the archive with all files.

If you run multibatch\_jpredapi.pl with the command line option -h you get a short help message.

`perl multibatch_jpredapi.pl -h`

If you have that set, you can run the following command
`perl multibatch_jpredapi.pl -e [insert your email adress here without the brackets] -f example_accnums.txt -d ./path/to/download_folder -j ./path/to/jpredapi -i ./path/to/fasta_files/ -r jnet:html:tar.gz`


# TODO

* Make verbose output make more readable.


# KNOWN ISSUES

* Restart on new day does not work jet.
* Log file does not support multiple running instances in the same folder.
* Log file gets crowded when the script is run many times from the same folder.


# Contribute

Any comment and contribution is very welcome and pull requests will be accepted if they contribute to the intended functionality of this repository.


# Acknowledgements

Without Alexey Drozdetskiy who currently maintains and develops JPred, this would not have been done. Thank you for the many emails with valuable information and inputs as well as added features to JPred to make this script more robust.

