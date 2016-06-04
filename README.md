# TMAC

Welcome to **TMAC**: A Toolbox of Modern Async-Parallel, Coordinate, Splitting, and Stochastic Methods


## Features

   * A rich set of predefined operators.
   * A set of predefined operator splitting schemes.
   * An asynchronous coordinate update framework.
   * A synchronous parallel update driver.
   * Options to load datasets in various format.
   * A rich set of applications build on top of TMAC.
   * Support for Matlab, Python and Julia (coming soon)


## Platforms
TMAC can been used on several platforms:

   * Linux
   * Windows
   * Mac OS X

## Requirements
TMAC is designed to have fairly minimal requirements to build. Currently, we support Linux, Windows, and Mac OS X.
If you notice any problems on your platform, please create an [issue](https://github.com/uclaopt/TMAC/issues).

### Linux and Mac OS X Requirements
   * GNU-compatible Make
   * gcc>=4.7
   * BLAS

## Build

Building TMAC can be as simple as:

```
make
```


## Use the Applications

We build a user-friendly interface to run TMAC for different applications through shell. You can run it through the following command:

```
./run_me.sh
```


## Contributing Code
We welcome patches. If you plan to contribute a patch, you need to write tests for any new code. Changes should be verified to not
break existing tests before they are submitted for review. We use Google test for unit testing. Our unit tests are in the test folder.
If you are adding tests to a new file, you will need to modify the Makefile to compile the source code, otherwise, nothing needs to be
changed in the Makefile. The following commands should build and run the unit tests.

```
make
./your_unittest
```


## Getting the Data

So far, TMAC support the following data format:
   * [Matrix Market Format](http://math.nist.gov/MatrixMarket/formats.html#MMformat)
   * [LIBSVM format](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/)

You can download some example datasets from [here](https://github.com/uclaopt/datasets)
You can also obtain the regression and classification datasets from the LIBSVM [website](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/).



## Troubleshooting

* You can report bugs through the [issue tab](https://github.com/uclaopt/TMAC/issues/new)

* fatal error: ```<omp.h>``` file not found
  * First make sure you are using the correct compiler, i.e., GCC >= 4.7 from the GNU Project. For OSX,
  please follow the instruction [here](http://stackoverflow.com/questions/20340117/omp-h-library-isnt-found-in-the-gcc-version-4-2-1-in-mavericks) to download and install gcc-4.9.
  For Ubuntu, you can follow this [link](http://askubuntu.com/questions/428198/getting-installing-gcc-g-4-9-on-ubuntu).

* install g++ without root privileges. This [link](http://luiarthur.github.io/gccinstall) is very helpful.

## Acknowledgement

We would like to acknowledge the [Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page) library, the [sparse BLAS](http://math.nist.gov/spblas/) library, and
[Google Test](https://github.com/google/googletest).


## Related Papers

```

@article{peng2015arock,
  title = {ARock: an Algorithmic Framework for Asynchronous Parallel Coordinate Updates},
  author = {Peng, Zhimin and Xu, Yangyang and Yan, Ming and Yin, Wotao},
  journal = {arXiv:1506.02396},
  year = {2015},
  publisher = {http://arxiv.org/abs/1506.02396}
}

@article{PengWuXuYanYin2016_coordinate,
  title = {Coordinate friendly structures, algorithms and applications},
  volume = {1},
  number = {1},
  journal = {Annals of Mathematical Sciences and Applications},
  author = {Peng, Zhimin and Wu, Tianyu and Xu, Yangyang and Yan, Ming and Yin, Wotao},
  month = jan,
  year = {2016},
  pages = {59--119}
}

```
