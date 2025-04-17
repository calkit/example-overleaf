# Overleaf integration example

A [Calkit](https://calkit.org) project that demonstrates
integrating with Overleaf to edit a publication,
while the rest of the project is responsible for processing data and
creating figures.
The publication can also be edited directly from this project repo,
and the `figures` directory
(configurable in the publication `overleaf` metadata in `calkit.yaml`)
is pushed to Overleaf so the paper
can be compiled there as well.

To sync (bidirectionally) with Overleaf, run:

```sh
calkit overleaf sync
```

The publication can then be rebuilt with:

```sh
calkit run
```

The Overleaf project was initially imported with:

```sh
calkit overleaf import \
    https://www.overleaf.com/project/68000059d42b134573cb2e35 \
    paper \
    --title "Paper 2" \
    --kind journal-article \
    --sync-path paper.tex \
    --push-path figures
```
