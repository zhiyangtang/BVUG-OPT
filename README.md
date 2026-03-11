# BVUG-OPT

1.'Appendix.pdf' contains the appendix of our paper, which includes some proofs that were omitted from the paper due to space constraints.

2.'BVUG-OPT_code' contains the source codes of our paper and sample datasets and queries. 
To run the codes, please read the following instructions.

## Datasets

We provide three datasets in the folder "Datasets/" for testing, D1 to D3.

If you want to use other datasets, please copy them into "Datasets/".

## Generate Queries

Usage of query generation program in "Datasets/GenQuery/":

```C++
cd Datasets/GenQuery/
make clean
make
./GenerateQueries <Graph File> <Number of queries>
cd ../../
```

- Graph File: input graph filename in "Datasets/"
- Number of queries: the number of random queries

You can edit the parameter θ in the code.

After executions, generated query files are stored as "Datasets/GenQuery/{Graph File}.query"

## Execute BVUG-OPT

Usage of BVUG-OPT main program in "STPG/":

```C++
cd STPG/
make clean
make
./Run <Graph File> <Query File>
cd ../
```

- Graph File: input graph filename in "Datasets/"
- Query File: input query filename in "Datasets/"

You can edit the parameter W in the code.

After executions, the logs including running time are written in "Results/Logs.csv"
