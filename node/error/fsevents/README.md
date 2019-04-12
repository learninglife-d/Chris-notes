# Error download(404) 

https://fsevents-binaries.s3-us-west-2.amazonaws.com

```
node-pre-gyp WARN Tried to download(404): https://fsevents-binaries.s3-us-west-2.amazonaws.com/v1.2.4/fse-v1.2.4-node-v67-darwin-x64.tar.gz 
node-pre-gyp WARN Pre-built binaries not found for fsevents@1.2.4 and node@11.13.0 (node-v67 ABI, unknown) (falling back to source compile with node-gyp) 
  SOLINK_MODULE(target) Release/.node
```
## Solution
Downgrade node version (10.15.3)