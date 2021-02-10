# podman-learn
My how to notes for Podman, Buildah and Skopeo


### Create a base image with Buildah 

This is the best method I think in a condition if you are starting with a project to run on containers in a ristricted environment where you cant pull images from a public container registry.

```
# container=$(buildah from scratch) 
# buildah containers
# echo $container
# mnt=$(buildah mount $container) 
# echo $mnt 
# dnf install --releasever=8 --installroot $mnt bash coreutils -y
# buildah run $container bash 
# buildah umount $container 
# buildah commit $container centos-minimum:latest 
# buildah images 
```
If not, and you got the luxury of direct internet access to pull the image, [Redhat Universal Base Image](https://developers.redhat.com/products/rhel/ubi) is a good stating point with **no ristrictions**. 

### Ref List:

[Everything You Need to Know About Buildah](https://dzone.com/articles/everything-you-need-to-know-about-buildah) 

[starting with containers building running and managing containers](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/building_running_and_managing_containers/starting-with-containers_building-running-and-managing-containers)

[how-does-rootless-podman-work](https://opensource.com/article/19/2/how-does-rootless-podman-work)

[podman-and-user-namespaces](https://opensource.com/article/18/12/podman-and-user-namespaces) 

[tips-tricks-rootless-buildah](https://opensource.com/article/19/3/tips-tricks-rootless-buildah) 

[Redhat Univarsal Base Image](https://developers.redhat.com/products/rhel/ubi) 

[container video series](https://www.redhat.com/sysadmin/container-video-series) 

[podman-managing-containers-pods](https://developers.redhat.com/blog/2019/01/15/podman-managing-containers-pods/?intcmp=701f20000012ngPAAQ) 

[container-terminology-practical-introduction](https://developers.redhat.com/blog/2018/02/22/container-terminology-practical-introduction/) 

[container-networking-podman](https://www.redhat.com/sysadmin/container-networking-podman) 

[privileged-flag-container-engines](https://www.redhat.com/sysadmin/privileged-flag-container-engines)

[podman-shareable-systemd-services](https://www.redhat.com/sysadmin/podman-shareable-systemd-services)

[rootless-containers-podman](https://www.redhat.com/sysadmin/rootless-containers-podman)

[7-transports-features](https://www.redhat.com/sysadmin/7-transports-features)

[podman-guides-2020](https://www.redhat.com/sysadmin/podman-guides-2020)

[basic-security-principles-containers](https://www.redhat.com/sysadmin/basic-security-principles-containers)

[behind-scenes-podman](https://www.redhat.com/sysadmin/behind-scenes-podman)

[podman-kubernetes-yaml](https://developers.redhat.com/blog/2019/01/29/podman-kubernetes-yaml/)

[how-to-install-wildfly-on-centos-8](https://www.liquidweb.com/kb/how-to-install-wildfly-on-centos-8/) 
