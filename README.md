## ADLBenchmark.jl
Pure Julia entry into the [ADL Benchmarks](https://github.com/iris-hep/adl-benchmarks-index).

[View the rendered notebook](https://moelf.github.io/ADLBenchmark.jl/)

## To develope
1. `git clone https://github.com/Moelf/HSF_Julia_Tutorial/`
2. `cd HSF_Julia_Tutorial/docs`
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
