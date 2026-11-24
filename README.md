# Camera and Scene Motion Interfere with Each Other in Video Representations

**Ziqi Zhou, Laura Sevilla-Lara** · School of Informatics, University of Edinburgh

![Paper](https://img.shields.io/badge/Paper-coming%20soon-lightgrey)
[![Project page](https://img.shields.io/badge/Project-Page-blue)](https://jia1018.github.io/Freeze/)
![Code](https://img.shields.io/badge/Code-coming%20soon-lightgrey)
![Benchmark](https://img.shields.io/badge/Freeze%20benchmark-coming%20soon-lightgrey)

<p align="center">
  <img src="docs/static/images/teaser.png" width="65%" alt="Two Something-Something v2 clips in which the object and the camera move together, misclassified by state-of-the-art video backbones">
</p>

Real-world videos often contain both camera motion and scene motion, and video foundation models encode the two jointly. We ask whether the two motions interfere with each other in these representations, and whether the interference can be reduced post hoc.

- **Freeze** is a synthetic benchmark of video triplets: the original clip, the same clip with the **camera frozen**, and the same clip with the **scene frozen**. It has an object subset (Freeze-Object, rendered physics scenes) and a human subset (Freeze-Human). All four video foundation models we test do better on every camera and scene task once the other motion is frozen, so the interference goes both ways.
- **CamBit** and **SceneBit** are two lightweight mappings learned on top of fixed backbone features. They bring a clip's features closer to its scene-frozen and camera-frozen versions. CamBit improves camera understanding and geometric grounding on real videos for nearly every task and backbone; SceneBit improves the scene tasks of Freeze and those on real videos, with a context-dependent effect.

<p align="center">
  <img src="docs/static/images/overview.png" width="65%" alt="Overview of the CamBit and SceneBit mappings">
</p>

## Citation

```bibtex
@inproceedings{zhou_freeze,
  title     = {Camera and Scene Motion Interfere with Each Other in Video Representations},
  author    = {Zhou, Ziqi and Sevilla-Lara, Laura},
  booktitle = {TBD},
  year      = {TBD}
}
```

## Acknowledgements

The project page is based on the [Nerfies](https://github.com/nerfies/nerfies.github.io) template.
