This is a project of Avy verifier and extra dependencies

To install/build
===============
BRANCH_NAME is one of dev, master, hwmcc15
 
  > git checkout -b LOCAL_NAME origin/BRANCH_NAME 

  > git submodule init

  > git submodule update

  > mkdir build ; cd build

  > cmake -DCMAKE_BUILD_TYPE=[Release|Debug] [-DAVY_STATIC_EXE=ON] ../

  > cmake --build .

The main executable is `build/avy/src/avy'

[Arie Gurfinkel](http://arieg.bitbucket.org) and [Yakir Vizel](http://www.cs.technion.ac.il/~yvizel/)

HWMCC'15
==============

1. Binary distribution [avy+fib](https://bitbucket.org/arieg/extavy/downloads/avy-hwmcc15-r2.tar.gz)

CAV'15
==============

To reproduce our experiments for CAV'15, follow these steps:

1. Binary distribution [avy+fib](https://bitbucket.org/arieg/extavy/downloads/fib_cav15.tar.gz)

1. HWMCC benchmarks [HWMCC'13](http://fmv.jku.at/hwmcc13/hwmcc13aigs.7z) [HWMCC'14](http://fmv.jku.at/hwmcc14cav/hwmcc14benchmarks.7z) [Intel](http://fmv.jku.at/hwmcc/hwmcc08intel.php)

1. navy <AIG file> --verbose=3  --min-suffix=1 --sat-simp=0 --itp-simp=0 --shallow-push=1 --reset-cover=1 --glucose --glucose_itp --opt-bmc=1

