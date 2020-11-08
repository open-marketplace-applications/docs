# Storage
Everything user-related is stored in the user's browser. Products need to be stored on a device that is 24/7 connected to the internet. 

## An Encrypted Data Vault

We store a significant amount of sensitive data online, such as personally identifying information (PII), trade secrets and customer information.


### Differences between Solid and IPFS

**Solid**
- File and graph store
- Spec requires no encyption
- Extended file metadata is supported
- Read/write protocol: REST (LDP)
- Auth: WebID-OIDC	
- Data locality: Server
- Replication: None
- Access Control: [Web Access Control (WAC)] (https://github.com/solid/web-access-control-spec)

**IPFS**
- Content-addressable distributed file store
- Spec requires no encyption
- Extended file metadata is not supported
- Read/write protocol: cli/HTTP
- Data locality: Public nodes
- Replication: [Peer to peer](https://discuss.ipfs.io/t/replication-on-ipfs-or-the-backing-up-content-model/372)
- Access Control: [None](https://github.com/ipfs/notes/issues/376)