# KindleGen Docker container

A light-weight (Alpine Linux based) [Docker](https://www.docker.io/) container image for [KindleGen](http://www.amazon.com/gp/feature.html?docId=1000765211). Has KindleGen set as the entrypoint.

This image is a fork of James Gregory's KindleGen Docker image. You can see the original image here: https://github.com/jagregory/kindlegen-docker

## Usage

    docker run emmanuelrosa/kindlegen

    *************************************************************
     Amazon kindlegen(Linux) V2.9 build 0730-890adc2
     A command line e-book compiler
     Copyright Amazon.com and its Affiliates 2013
    *************************************************************

    Usage : kindlegen [filename.opf/.htm/.html/.epub/.zip or directory] [-c0 or -c1 or c2] [-verbose] [-western] [-o <file name>]

A `/source` directory is created in the container, which can be mapped for use with relative file paths. kindlegen will always be run from the `/source` directory in the container.

    docker run -v `pwd`:/source jagregory/kindlegen input.epub

## NOTICE

Dowloading KindleGen typically requires agreement to terms of use. Obviously this image bypasses that need, but I recommend you review the [terms](http://www.amazon.com/gp/feature.html?docId=1000765211) anyway.
