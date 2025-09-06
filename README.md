# Qualcomm Docker Container with Access to Drivers

Please make sure you include additional devices when using this container.

```bash
docker run --device=/dev/kgsl-3d0 --device=/dev/dri ghcr.io/kastnerrg/qualcomm-docker-base
```