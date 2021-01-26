# podman-learn
My how to notes for Podman, Buildah and Skopeo


### Create a base image with Buildah 

This is the best method I think in a condition if you are starting with a project to run on containers in a ristricted environment where you cant pull images from a public container registry. [**Ref: 

```
# newcontainer=$(buildah from scratch) 
# buildah containers 
# scratchmnt=$(buildah mount $newcontainer) 
# echo $scratchmnt 
# dnf -y group install "Minimal Install" --releasever=8 --installroot=$scratchmnt 
# buildah umount $newcontainer 
# buildah run $newcontainer bash 
# buildah commit $newcontainer centos-minimum:latest 
# buildah images 
```

### Ref List:

[Everything You Need to Know About Buildah](https://dzone.com/articles/everything-you-need-to-know-about-buildah) 

(https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/building_running_and_managing_containers/starting-with-containers_building-running-and-managing-containers

https://opensource.com/article/19/2/how-does-rootless-podman-work 

https://opensource.com/article/18/12/podman-and-user-namespaces 

https://opensource.com/article/19/3/tips-tricks-rootless-buildah 

https://developers.redhat.com/products/rhel/ubi 

https://www.liquidweb.com/kb/how-to-install-wildfly-on-centos-8/ 
