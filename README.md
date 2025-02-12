# Advanced Bioinformatics for Next-Generation Sequencing 2022: Week 1




Day | Time |  Subject | Lecturer
--- | --- | --- | ---
Day 1 - Monday | 9:15 - 12 | NGS data - Workflow, formats and programs | Thorfinn Sand Korneliussen,<br/> Exercises: Isin Altinkaya
Day 2 - Tuesday | 13:15 - 16 | Mapping - Suffix arrays and Burrows-Wheeler Transform | Rasmus A. Henriksen
Day 3 - Friday | 9:15 - 12 | Uncertainty and exercise conclusions | Thorfinn/Rasmus/Abigail


# Getting started
## Connecting to the server via SSH


X11 forwarding method will allow you to start a graphical application on the remote system and forward this application's windows to your local system. We need to enable X11 forwarding to view the plots we will be generating for the exercises.

We use `-X` option to enable X11 forwarding over SSH:

```sh
$ ssh -X <your_username>@<server_name_or_ip>
```

Replace with your remote server username. For example:


```sh
$ ssh -X isin@ricco.popgen.dk
```




## Setting up the working environment


If you are working on the ricco server, and therefore will not be not clonning the repository, all commands in the following seven exercises will be relative to the base directory called `/TEACHING/BIOINF22/adv_binf_2022_week1`

```sh
day1
├── data
│   ├── alignment
│   ├── fasta
│   ├── fastq
│   ├── reference_fasta
│   └── reference_fasta_hs37d5
├── exercises
│   ├── alignment_formats
│   ├── mapdamage
│   ├── trimming
│   └── variant_call_format
├── Makefile
└── README.md
```

Git is a version-control system software for tracking changes in a set of files, and is useful for coordinating work among multiple people working in collaboration. GitHub is one of the most popular git repository hosting services. Git is not covered within the scope of this class, and will only be used for downloading the exercise materials. To learn more about git and GitHub, see [GithHub Lab](https://lab.github.com/) (optional).


```sh
$ git clone https://github.com/ANGSD/adv_binf_2022_week1
$ cd adv_binf_2022_week1/day1
# gunzip files
$ make unzip
# copy reference files
$ make copy
```

