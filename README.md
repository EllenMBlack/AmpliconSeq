# AmpliconSeq
wireless-nat-inside:macqiime_1.9.1-20150604_os10.7 ellen$ cd ~/Downloads/MacQIIME_1.9.1-20150604_OS10.7/
wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 ellen$ sudo cp scripts/macqiime /usr/local/bin/macqiime
wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 ellen$ sudo chmod a+x /usr/local/bin/macqiime
wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 ellen$ macqiime

MacQIIME version:
MacQIIME 1.9.1-20150604

Sourcing MacQIIME environment variables...

  This is the same as a normal terminal shell, except your default
  python is DIFFERENT (/macqiime/bin/python) and there are other new
  QIIME-related things in your PATH.

  Type "exit" (return) to go back to your normal shell

MacQIIME wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 $ join_paired_ends.py -f /users/ellen/desktop/ellenqiime/r1.fastq -r /users/ellen/desktop/ellenqiime/r2.fastq -b /users/ellen/desktop/ellenqiime/i1.fastq -o /users/ellen/desktop/ellenqiime/fastq-join_joined
MacQIIME wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 $ split_libraries_fastq.py -i/Users/ellen/Desktop/EllenQIIME/fastq-join_joined/fastqjoin.join.fastq -b /Users/ellen/Desktop/EllenQIIME/fastq-join_joined/fastqjoin.join_barcodes.fastq -m /Users/ellen/Desktop/EllenQIIME/Barcode_file.txt -o /Users/ellen/Desktop/EllenQIIME/slout --barcode_type 12
MacQIIME wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 $ pick_open_reference_otus.py -o /Users/ellen/Desktop/EllenQIIME/open_refs_otus -i /Users/ellen/Desktop/EllenQIIME/slout/seqs.fna -r /Users/ellen/Desktop/EllenQIIME/gg_13_5.fasta -a -O 2 -f
MacQIIME wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 $ filter_otus_from_otu_table.py -i /users/ellen/desktop/ellenqiime/open_refs_otus/otu_table_mc2_w_tax_no_pynast_failures.biom -o /users/ellen/desktop/ellenqiime/open_refs_otus/otu_table_filtered.biom --min_count_fraction 0.00005


MacQIIME wireless-nat-inside:MacQIIME_1.9.1-20150604_OS10.7 $ core_diversity_analyses.py -i /users/ellen/desktop/ellenqiime/open_refs_otus/otu_table_filtered.biom -o /users/ellen/desktop/ellenqiime/diversity -m /users/ellen/desktop/ellenqiime/barcode_file.txt -e 6000 -c Mussel,Depth,Day,Growth -a -O 2 -t /users/ellen/desktop/ellenqiime/open_refs_otus/rep_set.tre

