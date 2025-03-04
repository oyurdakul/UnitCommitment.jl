# UnitCommitment.jl

**UnitCommitment.jl** (UC.jl) is an optimization package for the Security-Constrained Unit Commitment Problem (SCUC), a fundamental optimization problem in power systems used, for example, to clear the day-ahead electricity markets. Both deterministic and two-stage stochastic versions of the problem are supported. The package provides benchmark instances for the problem, a flexible and well-documented data format for the problem, as well as Julia/JuMP implementations of state-of-the-art mixed-integer programming formulations and solution methods.

## Package Components

* **Data Format:** The package proposes an extensible and fully-documented JSON-based data specification format for SCUC, developed in collaboration with Independent System Operators (ISOs), which describes the most important aspects of the problem. The format supports all the most common generator characteristics (including ramping, piecewise-linear production cost curves and time-dependent startup costs), as well as operating reserves, price-sensitive loads, transmission networks and contingencies.
* **Benchmark Instances:** The package provides a diverse collection of large-scale benchmark instances collected from the literature, converted into a common data format, and extended using data-driven methods to make them more challenging and realistic.
* **Model Implementation**: The package provides a Julia/JuMP implementations of state-of-the-art formulations and solution methods for the deterministic and stochastic SCUC, including multiple ramping formulations ([ArrCon2000](https://doi.org/10.1109/59.871739), [MorLatRam2013](https://doi.org/10.1109/TPWRS.2013.2251373), [DamKucRajAta2016](https://doi.org/10.1007/s10107-015-0919-9), [PanGua2016](https://doi.org/10.1287/opre.2016.1520)), multiple piecewise-linear costs formulations ([Gar1962](https://doi.org/10.1109/AIEEPAS.1962.4501405), [CarArr2006](https://doi.org/10.1109/TPWRS.2006.876672), [KnuOstWat2018](https://doi.org/10.1109/TPWRS.2017.2783850)) and contingency screening methods ([XavQiuWanThi2019](https://doi.org/10.1109/TPWRS.2019.2892620)). Our goal is to keep these implementations up-to-date as new methods are proposed in the literature.
* **Benchmark Tools:** The package provides automated benchmark scripts to accurately evaluate the performance impact of proposed code changes.

## Table of Contents

```@contents
Pages = ["usage.md", "format.md", "instances.md", "model.md", "api.md"]
Depth = 3
```

## Authors
* **Alinson S. Xavier** (Argonne National Laboratory)
* **Aleksandr M. Kazachkov** (University of Florida)
* **Ogün Yurdakul** (Technische Universität Berlin)
* **Jun He** (Purdue University)
* **Feng Qiu** (Argonne National Laboratory)

## Acknowledgments

* We would like to thank **Yonghong Chen** (Midcontinent Independent System Operator), **Feng Pan** (Pacific Northwest National Laboratory) for valuable feedback on early versions of this package.

* Based upon work supported by **Laboratory Directed Research and Development** (LDRD) funding from Argonne National Laboratory, provided by the Director, Office of Science, of the U.S. Department of Energy under Contract No. DE-AC02-06CH11357

* Based upon work supported by the **U.S. Department of Energy Advanced Grid Modeling Program** under Grant DE-OE0000875.

## Citing

If you use UnitCommitment.jl in your research (instances, models or algorithms), we kindly request that you cite the package as follows:

* **Alinson S. Xavier, Aleksandr M. Kazachkov, Ogün Yurdakul, Feng Qiu**, "UnitCommitment.jl: A Julia/JuMP Optimization Package for Security-Constrained Unit Commitment (Version 0.4)". Zenodo (2022). [DOI: 10.5281/zenodo.4269874](https://doi.org/10.5281/zenodo.4269874).

If you use the instances, we additionally request that you cite the original sources, as described in the [instances page](instances.md).

## License

```text
UnitCommitment.jl: A Julia/JuMP Optimization Package for Security-Constrained Unit Commitment
Copyright © 2020-2023, UChicago Argonne, LLC. All Rights Reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted
provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of
   conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice, this list of
   conditions and the following disclaimer in the documentation and/or other materials provided
   with the distribution.
3. Neither the name of the copyright holder nor the names of its contributors may be used to
   endorse or promote products derived from this software without specific prior written
   permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR
IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY
AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.
```
