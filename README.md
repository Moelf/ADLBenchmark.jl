## ADLBenchmark.jl
Pure Julia entry into the [ADL Benchmarks](https://github.com/iris-hep/adl-benchmarks-index).

[View the rendered notebook](https://moelf.github.io/ADLBenchmark.jl/)

## Length of Code comparison
length (in chars) of function body after stripping spaces and line breaking, excluding plots and file opening etc.
big query has +3227 from utility functions

| Query # | Julia | RDataFrame | coffea | bigquery |
|:----------: |:---------:| :------------: | :--------: |:--------: |
| 1 |28| 81 | 261 |127 |
| 2 |93| 99 | 270 |152 |
| 3 |178| 289 | 295 |171 |
| 4 |126| 255 | 330 |186 |
| 5 |594| 1249 | 601 |411 |
| 6 |633| 2307 | 1231 |642 |
| 7 |683| 2216 | 663 |569 |
| 8 |1035| 3560 | 1526 |1665 |


## To develope
1. `git clone https://github.com/Moelf/ADLBenchmark.jl/`
2. `cd ADLBenchmark.jl`
3. `julia --project=.`

then:
```julia
julia> using Pkg

julia> Pkg.instantiate()

julia> using Pluto; Pluto.run(threads=6)
```

Then using the web GUI, open up `notebook.jl`. You will have to download the file (as mentioned in [ADL repo](https://github.com/iris-hep/adl-benchmarks-index/blob/master/README.md#input-data-files),
if you have `xrdcp` installed, you can run:
```bash
xrdcp --parallel 4 'root://eospublic.cern.ch//eos/root-eos/benchmark/Run2012B_SingleMu.root' ./
```

and you have to change the path in the `notebook.jl` accordingly.

## Note
- For some tasks, I have used multi-threading to reduce processing time.
- I have compared to [coffea](https://github.com/CoffeaTeam/coffea-benchmarks/tree/master) and [RDataFrame](https://github.com/root-project/opendata-benchmarks)
implementations result as cross check 
