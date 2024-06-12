# Seqera Containers

Containers have revolutionized research by providing portable environments that eliminate compatibility issues across different computing systems.

Nextflow has supported Docker containers for nearly a decade, but pipeline developers often face challenges in having to write Dockerfile scripts for each workflow step.

Projects like BioContainers offer pre-built images for Bioconda tools but have limitations. Wave, our open-source on-demand container provisioning service, simplifies this process by allowing Nextflow developers to reference conda packages or a bundled Dockerfile, building containers on the fly for specific local environments.

Seqera Containers enhance the Wave experience by allowing users to type in the names of desired tools and instantly receive a container URI, usable for any purpose. The image is stored in a cache provided by AWS, ensuring reproducibility and availability for future runs without expiry.

Users can:

- Request any combination of packages
- Select architecture and image format (i.e. linux/arm64 architecture)
- Users can create Singularity images and download `.sif` files directly

Clicking “View build details” for the container shows the full information of the Dockerfile, conda environment file, and build settings, as well as the complete build logs. Every container includes results from a security scan.

### TODO gif
