# Build It PureScript

bips wraps Pulp and simply forwards all arguments to Pulp, after running
`make -f prepare.make all` in all dependant and dependency roots that have a
`prepare.make` file. The makefiles must generate PureScript sources in the `gen`
directory relative to `prepare.make`. bips passes all these `gen` directories
to Pulp with the Pulp `-I` command-line option. Additionally
`make -f prepare.make clean` can be run by invoking `bips clean`.
