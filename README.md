pl-objectdetection
==================

Contributer
---
Haoyang Wang  haoyangw@bu.edu

Kefan   Zhang kefan29@bu.edu

Feel free to reach out us if you have any question. :)

Abstract
--------
The python scripts is forked from this repo provided by Nvidia:

https://github.com/NVIDIA/object-detection-tensorrt-example

and it's modified to use a file as the input, run on a cloud machine and become a chris plugin.

## Deploy requirement
Your host computer should be a linux os and installed CUDA 10.1 && nvidia container.

For ppc64le machine:

https://github.com/FNNDSC/pl-objectdetection_ppc64

For x86_64 machine:

https://github.com/FNNDSC/pl-objectdetection_x86

Run
---

### Using `docker run`

To run using `docker`, be sure to assign an "input" directory to
`/incoming` and an output directory to `/outgoing`. *Make sure that the*
`$(pwd)/out` *directory is world writable!*
And use the `--f` flag to set the inputfile inside your `/incoming` directory.

Now, prefix all calls with

``` {.sourceCode .bash}
docker run --security-opt label=type:nvidia_container_t    \
           -v $(pwd):/incoming:z -v $(pwd)/out:/outgoing:z \
           docker.io/fnndsc/pl-matrixmultiply_moc_ppc64    \
           objectdetection.py                               \
           -f animal360p.webm /incoming /outgoing
```


How it works
---

Under constructing ...
