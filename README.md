# Estimating the number of Immortal Mutants

## JSON

The directory for experiments is `microjson/test/`

The directory for data  is `data/microjson/`

## Apache Commons

We have 10 Java libraries collected from Apache commons.

1.  commons-csv-1.7-RC1 a227a1e2fb61ff5f192cfd8099e7e6f4848d7d43
2.  commons-collections-4.4-RC1 cab58b3a8093a2f6b84f12783a3fb358747310f7
3.  commons-compress-1.18-RC1 b95d5cde4c68640f886e3c6802384fae47408a37
4.  commons-configuration-2.5-RC1 dc00a04783ea951280ba0cd8318f53e19acb707f
5.  commons-dbcp-2.6.0-RC1 3e7fca08d3585aa7cf70045ee3ed607cbaf04baa
6.  commons-imaging-1.0-alpha1-RC3 6f04ccc2cf8c867298579c355c6d88fd74da3e7b
7.  commons-io-2.6-RC3 2ae025fe5c4a7d2046c53072b0898e37a079fe62
8.  commons-lang: LANG_3_8_RC1 9801e2fb9fcbf7ddd19221e9342608940d778f8c
9.  commons-math MATH_3_6_RC2 95a9d35e77f70ffc9bd5143880c236a760b42005
10. commons-net NET_3_6 163fe46c019f5184016207c247cdff30ee740ecc

We did the following: Get the mutants from each using `PIT 1.4.9`; next, each
mutant was evaluated using the original test suite. The results of this are
available under results.

results/commons-csv.mutations.xml 638
results/commons-collections.mutations.xml 8309
results/commons-compress.mutations.xml 9523
results/commons-configuration.mutations.xml 6166
results/commons-dbcp.mutations.xml 4187
results/commons-imaging.mutations.xml 11580
results/commons-io.mutations.xml 3246
results/commons-lang.mutations.xml 13057
results/commons-math.mutations.xml 47879
results/commons-net.mutations.xml 5697


others:

results/commons-beanutils.mutations.xml 2916
results/commons-cli.mutations.xml 732
results/commons-codec.mutations.xml 3972
results/commons-crypto.mutations.xml 723
results/commons-dbutils.mutations.xml 755
results/commons-digester.mutations.xml 1635
results/commons-email.mutations.xml 584
results/commons-exec.mutations.xml 525
results/commons-fileupload.mutations.xml 615
results/commons-pool.mutations.xml 1357
results/commons-validator.mutations.xml 2009
total 126105

Next, we chose 100 mutants from the surviving mutants, and classified them
using manual classification (two investigators). The results of manual
classification of the surviving mutants are under the classified directory.
Note that csv had only 116 mutants, and hence all mutants were classified.

   117 classified/commons-csv.sample.jh.csv
   117 classified/commons-csv.sample.sd.csv
   101 classified/commons-collections.sample.jh.csv
   101 classified/commons-collections.sample.sd.csv
   101 classified/commons-compress.sample.jh.csv
   101 classified/commons-compress.sample.sd.csv
   101 classified/commons-configuration.sample.jh.csv
   101 classified/commons-configuration.sample.sd.csv
   101 classified/commons-dbcp.sample.jh.csv
   101 classified/commons-dbcp.sample.sd.csv
   101 classified/commons-imaging.sample.jh.csv
   101 classified/commons-imaging.sample.sd.csv
   101 classified/commons-io.sample.jh.csv
   101 classified/commons-io.sample.sd.csv
   101 classified/commons-lang.sample.jh.csv
   101 classified/commons-lang.sample.sd.csv
   101 classified/commons-math.sample.jh.csv
   101 classified/commons-math.sample.sd.csv
   101 classified/commons-net.sample.jh.csv
   101 classified/commons-net.sample.sd.csv

classified: Note that the last updates by SD should be taken as ground truth.

We used Evosuite to generate test suites, and evaluate all the mutants
using these generated test suites. The results of these are available under

    ./evosuites/results/commons-csv.mutations.xml                        
    ./evosuites/results/commons-collections.mutations.xml
    ./evosuites/results/commons-compress.mutations.xml
    ./evosuites/results/commons-configuration.mutations.xml
    ./evosuites/results/commons-dbcp.mutations.xml
    ./evosuites/results/commons-imaging.mutations.xml
    ./evosuites/results/commons-io.mutations.xml
    ./evosuites/results/commons-lang.mutations.xml
    ./evosuites/results/commons-math.mutations.xml
    ./evosuites/results/commons-net.mutations.xml

We also used Randoop to generate test suites, and evaluate all the mutants
using the generated test suites.

    ./randoopsuites/results/commons-csv.mutations.xml                        
    ./randoopsuites/results/commons-collections.mutations.xml
    ./randoopsuites/results/commons-compress.mutations.xml
    ./randoopsuites/results/commons-configuration.mutations.xml
    ./randoopsuites/results/commons-dbcp.mutations.xml
    ./randoopsuites/results/commons-imaging.mutations.xml
    ./randoopsuites/results/commons-io/ (multiple)
    ./randoopsuites/results/commons-lang.mutations.xml
    ./randoopsuites/results/commons-math.mutations.xml
    ./randoopsuites/results/commons-net.mutations.xml