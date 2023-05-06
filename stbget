#!/bin/bash

# variables
FILE_PATH=$HOME"/stable-diffusion-webui/models/"

# check args
if [ $# -ne 2 ]; then
    echo "Invalid argument." 1>&2
    echo "Requires 3 arguments." 1>&2
    exit 1
fi

if [[ ! $1 =~ (http|https)://* ]]; then
    echo "Invalid params." 1>&2
    echo "Prams 1 is URL." 1>&2
    exit 1
fi

if [ ! -e $FILE_PATH$2 ]; then
    echo "Invalid params." 1>&2
    echo $2" is not found." 1>&2
    echo "This command requires 'stable-diffusion-webui' directory in your home directory." 1>&2
    exit 1
fi

# wget
wget -P $FILE_PATH$2/ $1 --content-disposition