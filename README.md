# bioinformatics-environment
Describe the environment used for bioinformatics

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


