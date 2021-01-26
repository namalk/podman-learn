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

[how-to-install-wildfly-on-centos-8](https://www.liquidweb.com/kb/how-to-install-wildfly-on-centos-8/) 
