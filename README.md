<div align="center">
  <img src="./images/LogoVinDrLab.png"/>
  <p><strong>The VinDr Lab</strong> is a Data Platform for Medical AI that enables building high-quality datasets and algorithms with lean process and advanced annotation features. The software is provided by the <a href="https://vindr.ai/">Medical Imaging team</a> at <a href="https://vinbigdata.org/">Vingroup Big Data Institute (VinBigdata)</a>.</p>
</div>
<p align="center">
  <a href="https://gitter.im/vindr-lab/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge">
    <img alt="Gitter" src="https://badges.gitter.im/vindr-lab/community.svg" />
  </a>
  <a href="/">
    <img alt="MIT License" src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" />
  </a>
</p>
<br/>

![Screeshot](./docs/img/vinlab_screenshot.png)
## About

VinDr Lab is a open-source platform for medical image annotation. 
It has been developed to remove the ground-truth barrier AI teams met to build meaningful medical AI applications. 
VinDr Lab provides a high-level web-interface equibbed with advanced annotation tools and project management features.

You can read more about the platform on
[vindr.ai/vindr-lab](https://vindr.ai/vindr-lab).

## What's here

This repo is the "master" repo for all VinDr Lab-related projects. 
It hosts the documentation and other misc. resources for VinDr Lab. 
Code for other projects, like backend and frontend, are hosted in other repositories. 

## Project Index 

All VinDr Lab projects and repositories underneath the VinBigdata Medical GitHub organization are listed here. To learn more about each project, see the README in each repository.

| Repository | Description | Maintainers |
|------------|-------------|-------------|
| [vinbigdata-medical/vinlab-sites](https://github.com/vinbigdata-medical/vinlab-sites) | Documentation and other general resources related to VinDr Lab | [@lego1st](https://github.com/lego1st), [@fuzzysource](https://github.com/fuzzysource) |
| [vinbigdata-medical/vindr-lab-deployment](https://github.com/vinbigdata-medical/vindr-lab-deployment) | Getting started with VinDr Lab. We support Kubernetes or Docker deployments. | [@iamatsundere](https://github.com/iamatsundere) |
| [vinbigdata-medical/vindr-lab-api](https://github.com/vinbigdata-medical/vindr-lab-api) | Middleware layer between user interface and backend systems | [@iamatsundere](https://github.com/iamatsundere) |
| [vinbigdata-medical/vindr-lab-id-generator](https://github.com/vinbigdata-medical/vindr-lab-id-generator) | For each study or task of a project, this service generates a new integer value which based on the key as string. | [@iamatsundere](https://github.com/iamatsundere) |
| [vinbigdata-medical/vindr-lab-uploader](https://github.com/vinbigdata-medical/vindr-lab-uploader) | Uploader modifies and transfers the DICOM files to database. | [@iamatsundere](https://github.com/iamatsundere) |
| [vinbigdata-medical/vindr-lab-viewer](https://github.com/vinbigdata-medical/vindr-lab-viewer) | Frontend: Viewer allows the manipulation, annotation, and serialization of observations and many more features. | [@HoAnhVan](https://github.com/HoAnhVan) |
| [vinbigdata-medical/vindr-lab-dashboard](https://github.com/vinbigdata-medical/vindr-lab-dashboard) | Frontend: Dashboard support data management and labeling administration | [@HoAnhVan](https://github.com/HoAnhVan) |


Note: Another way to find all VinDrLab-related repos is to go to Vinbigdata Medical GitHub mainpage and enter the search term "vindr-lab", like [here](https://github.com/vinbigdata-medical?utf8=%E2%9C%93&q=vindr-lab&type=&language=). 

## Documentation

Project documentation is hosted on
[our github page](https://vinbigdata-medical.github.io/vindr-lab/). We are hoping to
establish a more user-friendly version soon.

## Contributing

For quick questions there's no need to open an issue as you can reach us on [Gitter](https://gitter.im/vindr-lab/community).

If you're an experienced dev and interested in contributing to VinDr Lab:

* Please read our [Contribution guidelines](https://github.com/vinbigdata-medical/vindr-lab/blob/master/CONTRIBUTING.md) 
for details on what and how you can contribute.
* Check out our [Development Project Board]() for Product Roadmap.
* Look for tasks under the Issues tab in each repo.
* Join our [Gitter channel](https://gitter.im/vindr-lab/community).

## Acknowledgement

**Note:** If you use or find this repository helpful, please take the time to star this repository on Github. This is an easy way for us to assess adoption and it can help us obtain future funding for the project.

This work is supported primarily by [Vingroup Big Data Institute](http://vinbigdata.org/)
## License

[MIT License](https://github.com/vinbigdata-medical/vindr-lab/blob/master/LICENSE)
