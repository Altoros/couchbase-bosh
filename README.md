# MongoDB deployment for BOSH

This MongoDB deployment is intended for use with
[BOSH](https://github.com/cloudfoundry/bosh) deployment. Using this
you can easily create and scale your MongoDB cluster

## How does it help?

Using this release you can create MongoDB cluster in no time

## Who can benefit from it?

- Developers that want to test application with MongoDB cluster
  support
- System Administrators / DevOps because they create and reshape
  clusters easily

## What are the use cases?

- Creating replicated cluster
- Adding production cluster service for CloudFoundry (TBD)
- Created production sharded cluster (TBD)

## How to use it

1. For start you should install BOSH. You can find examples
[here](http://docs.cloudfoundry.com/docs/running/deploying-cf/). For
use this method you don't need to install CloudFoundry, you just need
small part of CloudFoundry (message bus).

2. Create manifest for your MongoDB cluster. You can find example in
   `examples` subdirectory.

3. Upload release to BOSH. You can do this using `bosh upload release releases/<last-release-number>`

4. Deploy cluser using manifest:
    1. `bosh deployment <your deployment file>` - selects deployment file to upload
    2. `bosh deploy` - applies deployment manifest to cluster.

5. When it finish installation, you can check nodes addresses using
`bosh vms`

## Roadmap

- Integration with CloudFoundry (adding service)
- Creating service for CloudFoundry
- Reshaping cluster

## Collaborate

You are welcome to contribute via
[pull request](https://help.github.com/articles/using-pull-requests).
