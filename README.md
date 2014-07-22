##g_distMat
***

###About

This tool is similar to gromacs tool g_mdmat. It calculates average distance matrix and other related matrices between two atom-groups from molecular dynamics trajectory (GROMACS, NAMD or AMBER).

##### Features

* Average minimum residues-distance matrix between two atom-groups that may be identical or different.
* Variance Matrix.
* Standard Deviation matrix.
* Fraction contact-map with the given cut-off distance.
* Fast -- multi-threading to use more than one core of the multi-core processor.

***

###Requirements
To compile and install, GROMACS libraries <code> libgmx, libmd, libgmxana </code> are required.
***

###Download
<pre><code>git clone https://github.com/rjdkmr/g_distMat
</code></pre>
***

###Installation
<pre><code>cd g_distMat
mkdir build
cd build
cmake ..  -DGMX_PATH=/opt/gromacs -DCMAKE_INSTALL_PREFIX=/opt/g_distMat
make
make install
</code></pre>

Directory <code>/opt/gromacs</code> should contains <code>include</code> and <code> lib </code> directories. If these directories are in seprate locations, use followings:
<pre><code>cmake ..  -DGMX_LIB=/path/to/lib -GMX_INCLUDE=/path/to/include -DCMAKE_INSTALL_PREFIX=/opt/g_resid_distrib
</code></pre>

If fftw library <code> libfftw3f.so or libfftw3f.a </code> are not present in standard locations:
<pre><code>-DFFTW_LIB=/path/to/fftw3/lib</code></pre>
***

###Usage
<pre><code>g_distMat -h
</code></pre>
***
