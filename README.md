# bioinformatics-environment
Describe the environment used for bioinformatics

## R environment
### set R environment
```
.libPaths()  # shows the $R_LIBS and $R_LIBS_USER
.Library
.Library.site
Sys.getenv() # keep an eye on "R_LIBS", "R_LIBS_USER", "R_LIBS_SITE"
```
if you happened to see "Warning in install.packages(...) : 'lib = "/usr/lib64/R"' is not writable"
then you can install R packages as follow:
```
install.packages("Rgraphviz", lib="/path/to/install")
BiocManager::install("Rgraphviz", lib="/path/to/install")
```
Besides, you can change the R environment to solve this once for all.
```
touch ~/.Renviron
R_LIBS=/path
R_LIBS_USER=/path
R_LIBS_SITE=path
```
## conda environment
### set conda channels
```
conda config --add channels conda-forge
conda config --add channels bioconda
conda config --add channels r
conda config --add channels default
conda config --set show_channel_urls yes
```
### set conda proxy
```
conda config --set proxy_servers.http http://[username]:[password]@[proxy-server]:[port]
conda config --set proxy_servers.https http://[username]:[password]@[proxy-server]:[port]
```
## pip environment
### set pip proxy
```
pip install --proxy http://[username]:[password]@[proxy-server]:[port] <pkgname>
```

## docker environment
### set docker proxy
```
export http_proxy=http://[username]:[password]@[proxy-server]:[port]
export https_proxy=http://[username]:[password]@[proxy-server]:[port]
```

## git environment
### set git proxy
```
git config --global http.proxy http://[username]:[password]@[proxy-server]:[port]
git config --global https.proxy http://[username]:[password]@[proxy-server]:[port]
```


