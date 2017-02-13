Why Hadoop over HPC(High performance Computing)

->negligible differences in terms of hardware (like InfiniBand vs. 1/10GigE) used, the main difference between HPC and Hadoop—well, actually MapReduce and feel free to replace it with Spark as well—is that of data locality.

->Hadoop also does seems to do the same thing which HPC does, which means solving that ‘big problem’. But we do this in a fundamentally different way. In the case of HPC, we assume that a ‘big problem’ can be solved by an equally ‘big computing machine’. But in case of Hadoop, we believe that the big problem can be divided into multiple sub-problems and those sub-problems can be solved by multiple small machines (or our commodity hardware). So, we assume that as the problem size increases, the number of the sub-problems increase. And as the number of sub-problems increase, the number of small machines (commodity hardware) to solve them also increase.

->Scenario-Turns out that when your dataset has, say, 1.5PB and the code to process it (for example a bunch of MapReduce jobs) has 1.5 MB, then it's more efficient to send the code to the data—residing on each node, which does both storage and compute—then the other way round, as seen in HPC.
