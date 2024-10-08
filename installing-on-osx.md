# Installing TF on OSX

This was more of a pain than I expected, so here is what worked for me.
General instructions can be found [here](https://developer.apple.com/metal/tensorflow-plugin/) but they don't mention that 3.10 is the newest compatible version of python.


## Step 1
Install conda and make a new environment.  I named mine `cst463`

## Step 2
Start your new environment

```shell
(base)
[Sun Oct  6 21:12:51 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ conda activate cst463
(cst463)
[Sun Oct  6 21:12:51 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$
```

## Step 3

Ensure that you are running a compatible version of python.  (This was the major pain point)

```shell
(cst463)
[Sun Oct  6 21:13:46 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ conda install python=3.10
```


### Step 4

Install Tensorflow Dependencies from the apple channel

```shell

(cst463)
[Sun Oct  6 21:14:23 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ conda install -c apple tensorflow-deps
Channels:
 - apple
 - defaults
Platform: osx-arm64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /Users/ssogden/miniconda3/envs/cst463

  added / updated specs:
    - tensorflow-deps


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    matplotlib-base-3.8.4      |  py310h46d7db6_0         6.8 MB
    pyparsing-3.0.9            |  py310hca03da5_0         151 KB
    ------------------------------------------------------------
                                           Total:         6.9 MB

....

```

### Step 5

Install tensorflow itself.

Note: as part of my ongoing role of throwing shade at big companies, apple is suggesting doing this through pip which is not necessarily the best approach.
There's a reason why we use conda.


```shell
(cst463)
[Sun Oct  6 21:15:07 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ python -m pip install tensorflow
Collecting tensorflow
  Downloading tensorflow-2.17.0-cp310-cp310-macosx_12_0_arm64.whl.metadata (4.1 kB)
Collecting absl-py>=1.0.0 (from tensorflow)
  Using cached absl_py-2.1.0-py3-none-any.whl.metadata (2.3 kB)
  
......
```


### Step 6

Install tensorflow-metal

```shell
(cst463)
[Sun Oct  6 21:17:13 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ python -m pip install tensorflow-metal
Collecting tensorflow-metal
  Downloading tensorflow_metal-1.1.0-cp310-cp310-macosx_12_0_arm64.whl.metadata (1.2 kB)
Requirement already satisfied: wheel~=0.35 in /Users/ssogden/miniconda3/envs/cst463/lib/python3.10/site-packages (from tensorflow-metal) (0.44.0)
Requirement already satisfied: six>=1.15.0 in /Users/ssogden/miniconda3/envs/cst463/lib/python3.10/site-packages (from tensorflow-metal) (1.16.0)
Downloading tensorflow_metal-1.1.0-cp310-cp310-macosx_12_0_arm64.whl (1.4 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.4/1.4 MB 14.5 MB/s eta 0:00:00
Installing collected packages: tensorflow-metal
Successfully installed tensorflow-metal-1.1.0

```


### Step 7

Install Keras

```shell
(cst463)
[Sun Oct  6 21:20:25 2024]
/Users/ssogden/repos/classes/CST463-assignments/labs/week07
$ conda install keras
Channels:
 - defaults
Platform: osx-arm64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /Users/ssogden/miniconda3/envs/cst463

  added / updated specs:
    - keras


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    absl-py-2.1.0              |  py310hca03da5_0         198 KB
    h5py-3.11.0                |  py310haafd478_0         1.2 MB
    keras-3.4.1                |  py310hca03da5_0         2.2 MB
    markdown-it-py-2.2.0       |  py310hca03da5_1         114 KB
    mdurl-0.1.0                |  py310hca03da5_0          19 KB
    ml_dtypes-0.4.0            |  py310h46d7db6_0         142 KB
    namex-0.0.7                |  py310hca03da5_0          14 KB
    optree-0.12.1              |  py310h48ca7d4_0         293 KB
    rich-13.7.1                |  py310hca03da5_0         505 KB
    ------------------------------------------------------------
                                           Total:         4.7 MB

The following NEW packages will be INSTALLED:

  absl-py            pkgs/main/osx-arm64::absl-py-2.1.0-py310hca03da5_0
  h5py               pkgs/main/osx-arm64::h5py-3.11.0-py310haafd478_0
  keras              pkgs/main/osx-arm64::keras-3.4.1-py310hca03da5_0
  markdown-it-py     pkgs/main/osx-arm64::markdown-it-py-2.2.0-py310hca03da5_1
  mdurl              pkgs/main/osx-arm64::mdurl-0.1.0-py310hca03da5_0
  ml_dtypes          pkgs/main/osx-arm64::ml_dtypes-0.4.0-py310h46d7db6_0
  namex              pkgs/main/osx-arm64::namex-0.0.7-py310hca03da5_0
  optree             pkgs/main/osx-arm64::optree-0.12.1-py310h48ca7d4_0
  rich               pkgs/main/osx-arm64::rich-13.7.1-py310hca03da5_0


Proceed ([y]/n)? y


Downloading and Extracting Packages:

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
```




