# JPred scheduler script

This Git repository contains a Perl script which can be used to run many JPred predictions with just one command.


## Requirements:

* Working JPred REST API on the system

You can get it from the official [JPred website](http://www.compbio.dundee.ac.uk/jpred4/api.shtml)

# How To

First you need a list of UniProt accession numbers in a file. One per line. Example (./example_accnums.txt):

    P09867
    P63323
    Q923U9

Then you need fasta files of the above accession numbers in one folder (./example\_fasta\_files/).

Next you can choose which files from the prediction you want to download. Concatenate all file type ending you want to download separated by a colon ':'. The default is to download the archive with all files.

If you run multibatch\_jpredapi.pl with the command line option -h you get a short help message.

`perl multibatch_jpredapi.pl -h`

If you have that set, you can run the following command
`perl multibatch_jpredapi.pl -e [insert your email address here without the brackets] -f example_accnums.txt -d ./path/to/download_folder -j ./path/to/jpredapi -i ./path/to/fasta_files/ -r jnet:html:tar.gz`


# ToDo

* Make verbose output more readable.


# Known Issues

* Log file does not support concurrently running instances in the same folder.
* Log file gets crowded when the script is run many times from the same folder.


# LICENSE

The original work 'multibatch_jpredapi.pl' and the JPred output is licensed under [GNU General Public License version 3](http://www.gnu.org/licenses/gpl-3.0.html) while the FASTA files are derived from UniProt and are licensed with the [Creative Commons Attribution-NoDerivs](https://creativecommons.org/licenses/by-nd/3.0/) license.


# Contribute

Any comment and contribution is very welcome and pull requests will be accepted if they contribute to the intended functionality of the repository.


# Acknowledgements

Dr. Alexey Drozdetskiy who currently maintains and develops JPred4 at the University of Dundee encouraged me to publish this script. My gratitude goes to him for the many emails with valuable information and inputs as well as added features to JPred4 to make this script more useful and robust.

