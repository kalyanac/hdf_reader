# hdf_reader
A sample reader that reads any hdf5 data file.
The reader has support for MPI as well. 

The reader iterates through all datasets and attributes within the dataset within the top group. Allocates necessary storage and reads the data. 

it reports timing and IO throughput observed. 

## Build
### without mpi

Use h5cc if you have it available. Pass -UMPIK to the compiler. 

###with MPI
Use h5cc, if it supports MPI. If not, provide hdf include and lib path to the equivalent of mpicc on your system. Pass -DMPIK to turn on MPI code. 

HDF can be downloaded here: [hdfgroup.org](hdfgroup.org)
MPI reference implementation is available here: [www.mpich.org](http://www.mpich.org/)
