# Mangaloid Glossary

A list of terms and their meanings for the [mangaloid
project](https://github.com/a-manga-thing), \#mangaloid on IRC. This is not a
spec, these definitions are only here to build consensus. Try to be as
non-prescriptive as possible when defining terms.

## General terms

- Gallery - A collection of image files <!-- Using gallery as it does not imply
  the existence of a parent (chapters imply that there is a parent manga title)
  -->
- Metadata - Information that includes, but is not limited to:
  - The location of a particular filesystem.
  - The location of a file in a filesystem.
  - A list of galleries.
  - What files a gallery contains.
  - Context specific information. For example:
    - A list of manga titles.
    - What galleries are associated to a manga.
    - Authors, artists, tags, etc.
- Instance - Hosts a database of metadata (and only metadata).
- Node - An IPFS server hosting files. It hosts a gateway.
- Front-end - A webserver hosting a website that lists galleries.


## Node

- (IPFS HTTPS) Gateway - A webserver that pulls files from IPFS as needed and
  serves them over HTTPS.
  
### Implementation details

Nodes have very little control over what files they serve, only what they decide
to keep in local storage (not cache).


## Instance

- Discovery protocol - Structured communication between instances that conveys:
  - Basic information about the instance (emergency/DMCA contact, name, status).
  - A summary of the metadata that the instance hosts.
  - A list of nodes that the instance is aware of (might be useful for network
  resiliency).
- Instance API - A REST API for others to access instance metadata.

### Implementation details

Instances have full control over the metadata they host.


## Front-end

- Instance index - A list of instances that the front-end is aware of.
- Node index - A list of nodes that the front-end is aware of.

### Implementation details

The front-end crawls its instance index for gallery metadata and presents them
to the user. When the user selects a gallery, it uses the metadata to download
the gallery files onto the users device from the specified node in the node
index.


## File storage

- Filesystem (FS) - A method for storing static data.
- IPFS - A distributed (peer-to-peer) filesystem.
- (Cryptographic) Hash - An (essentially) unique identifier for a file.
  Generated using a cryptographic hash function.
