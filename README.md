# Results

Results based on our production application


| Method                                                | Build time (s) | Size (mb) | Base image size (mb) | Added size (mb) |
|-------------------------------------------------------|----------------|-----------|----------------------|-----------------|
| [Naive](docker/Dockerfile1)                           |             53 |       896 |                  676 |             220 |
| [Separate install](docker/Dockerfile2)                |             28 |       896 |                  676 |             220 |
| [Multistage - separate test](docker/Dockerfile3)      |             28 |       790 |                  676 |             114 |
| [Multistage - copy to final](docker/Dockerfile4)      |             32 |       774 |                  676 |              98 |
| [Multistage - copy to alpine](docker/Dockerfile5)     |             33 |       166 |                   68 |              98 |
| [Multistage - copy to distroless](docker/Dockerfile6) |             33 |       173 |                   75 |              98 |

# Resources

https://learnk8s.io/blog/smaller-docker-images
