# podman-learn
My how to notes for Podman, Buildah and Skopeo


### Create a base image with Buildah 

This is the best method I think in a condition if you are starting with a project to run on containers in a ristricted environment where you cant pull images from a public container registry.

```
newcontainer=$(buildah from scratch) 
buildah containers 
scratchmnt=$(buildah mount $newcontainer) 
echo $scratchmnt 
dnf -y group install "Minimal Install" --releasever=8 --installroot=$scratchmnt 
buildah umount $newcontainer 
#buildah run $newcontainer bash 
buildah commit $newcontainer centos-minimum:latest 
buildah images 
```

[**Ref](https://www.server-world.info/en/note?os=CentOS_8&p=buildah&f=2)
