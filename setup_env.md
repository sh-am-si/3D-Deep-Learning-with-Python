# 1. Install GCC 13 and G++ 13 into your environment
conda install -c conda-forge gcc_linux-64=13 gxx_linux-64=13 -y

# 2. Re-set the variables to point to these new compilers
export CC=$CONDA_PREFIX/bin/x86_64-conda-linux-gnu-gcc
export CXX=$CONDA_PREFIX/bin/x86_64-conda-linux-gnu-g++
export CUDA_HOME=$CONDA_PREFIX
export FORCE_CUDA=1

# 3. Try the install again
pip install "git+https://github.com/facebookresearch/pytorch3d.git" --no-build-isolation