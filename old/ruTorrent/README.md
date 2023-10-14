# ruTorrent

This application is meant to be deployed to Kubernetes using Kustomize.

* **Website**: https://github.com/Novik/ruTorrent
* **Container Image:** https://hub.docker.com/r/linuxserver/rutorrent

<hr>

## Notes

* The container image requires the volume mounted files to be owned by a single `UID` and `GID` which is set in the Kustomization.yml file.

<hr>

## Instructions

An example overlay is provided from my environment. Simply create a new overlay using it as an example and deploy it to your environment like so:

   ```bash
    kustomize build ruTorrent/overlays/example | kubectl apply -f-
   ```

Start the pod and let ruTorrent intialize the configuration directory. Shut it down and move `rtlocal.rc` into place at `rtorrent/data/`. Restart the pod to apply your configuration file. 
