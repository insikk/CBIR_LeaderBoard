# CBIR_LeaderBoard
LeaderBoard for various CBIR models

Content-based Image Retrieval models.

Any suggestion for new benchmark dataset is welcome. 
Any suggestion for missing models is welcome. 

Most models are based on publicaly published result (peer-reviewd) or reproducable result (with source-code). 

If you have your model that is not published yet, and not open-sourced, I'll mark it in `etc` column.

Rank is based on Oxford105k (mid-scale image retrieval).:trophy:

# Oxford 5k, Paris 6k, Oxford 105k, Paris 106k, Holidays (mAP)

<table class="blueTable">
<thead>
<tr>
<th>model</th>
<th>oxf5k</th>
<th>par6k</th>
<th>oxf105k</th>
<th>par106k</th>
<th>holidays</th>
<th>yymm</th>
<th>ref</th>
<th>etc</th>
</tr>
</thead>
<tbody>
  

<tr>
<td>:trophy:GeM(Res)</td>
<td>87.8</td>
<td>92.7</td>
<td>84.6</td>
<td>86.9</td>
<td>93.9</td>
<td>17.11</td>
<td>[GeM17]</td>
<td>&nbsp;</td>
</tr>

<tr>
<td>GeM(VGG)</td>
<td>87.9</td>
<td>87.7</td>
<td>83.3</td>
<td>81.3</td>
<td>89.5</td>
<td>17.11</td>
<td>[GeM17]</td>
<td>&nbsp;</td>
</tr>


<tr>  
<td>R-MAC(Res,E2E)</td>
<td>86.1</td>
<td>94.5</td>
<td>82.8</td>
<td>90.6</td>
<td>94.8</td>
<td>16.10</td>
<td>[DeepIR16]</td>
<td>&nbsp;</td>
</tr>

<td>BoW(200k)+VV</td>
<td>80.1</td>
<td>73.4</td>
<td>74.5</td>
<td>64.9</td>
<td>-</td>
<td>16.xx</td>
<td>[VV16]</td>
<td>HesAff+RootSIFT, HE, VBW, Top1000, 1-to-1</td>
</tr>

<td>BoW(200k)</td>
<td>76.2</td>
<td>71.2</td>
<td>66.4</td>
<td>60.2</td>
<td>-</td>
<td>16.xx</td>
<td>[VV16]</td>
<td>&nbsp;</td>
</tr>


<td>BoW(16M,L16)+FSM</td>
<td>74.2</td>
<td>74.9</td>
<td>67.4</td>
<td>67.5</td>
<td>74.9</td>
<td>12.xx</td>
<td>[VW16M12]</td>
<td>HesAff+SIFT, 15 alt.words</td>
</tr>

<td>BoW(1M)+FSM</td>
<td>66.4</td>
<td>-</td>
<td>54.1</td>
<td>-</td>
<td>-</td>
<td>07.xx</td>
<td>[FSM07]</td>
<td>HesAff+SIFT</td>
</tr>


<td>BoW(1M)</td>
<td>61.8</td>
<td>-</td>
<td>49.0</td>
<td>-</td>
<td>-</td>
<td>07.xx</td>
<td>[FSM07]</td>
<td>&nbsp;</td>
</tr>

</tbody>
</table>

* This result does not use Query Expansion (QE), Database Augmentation (DBA), or Spatial Verification.
* For BoW based Image Retrieval System, Spatial Verifiaction is necessary to consider spatial information. So, I explicitly add the spatial verification method after `+` symbol. (i.e FSM, VV)
* HesAff: Hessian Affine Keypoint Detector. See [HesAff09]
* HE: Hamming Embedding (mitigate quantizatin error of visual words). See [HE08]
* RootSIFT: practical tip. better represenation for L2 distance measure. See [RootSIFT12]
* VBW: Visual Burstiness Weighting (mitigate repetative pattern dominancy problem). See [VBW09]
* TopXXX: Rerank top xxx results with spatial verification
* 1-to-1 : enforcing 1-to-1 correspondence with keypoint geometry. See [PGM15]


[GeM17]: Fine-tuning CNN Image Retrieval with No Human Annotation by Filip Radenović, Giorgos Tolias, Ondřej Chum https://arxiv.org/abs/1711.02512, 

[DeepIR16]: End-to-end Learning of Deep Visual Representations for Image Retrieval
 by Albert Gordo, Jon Almazan, Jerome Revaud, Diane Larlus https://arxiv.org/abs/1610.07940


[VV16]: A Vote-and-Verify Strategy for Fast Spatial Verification in Image Retrieval by Sch\"{o}nberger, Johannes Lutz and Price, True and Sattler, Torsten and Frahm, Jan-Michael and Pollefeys, Marc https://github.com/vote-and-verify/vote-and-verify

[RootSIFT12]: Three things everyone should know to improve object retrieval by Relja Arandjelovi´c Andrew Zisserman https://www.robots.ox.ac.uk/~vgg/publications/2012/Arandjelovic12/arandjelovic12.pdf


[PGM15]: Pairwise Geometric Matching for Large-scale Object Retrieval by Xinchao Li, Martha Larson, Alan Hanjalic https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Li_Pairwise_Geometric_Matching_2015_CVPR_paper.pdf

[VW16M12]: Learning Vocabularies over a Fine Quantization by Andrej Mikul´ık, Michal Perdoch, Ondˇrej Chum, and Jiˇr´ı Matas http://cmp.felk.cvut.cz/~perdom1/papers/mikulik_ijcv12.pdf



[HesAff09]: Efficient Representation of Local Geometry for Large Scale Object Retrieval by Perdoch, M. and Chum, O. and Matas, J. http://cmp.felk.cvut.cz/~perdom1/hesaff/

[VBW09]: On the burstiness of visual elements by  Herve Jegou ;  Matthijs Douze ;  Cordelia Schmid http://ieeexplore.ieee.org/abstract/document/5206609/

[HE08]: Hamming embedding and weak geometric consistency for large scale image search by Herve Jegou, Matthijs Douze, and Cordelia Schmid https://hal.inria.fr/inria-00316866/document/

[FSM07]: Object retrieval with large vocabularies and fast spatial matching by  James Philbin ;  Ondrej Chum ;  Michael Isard ;  Josef Sivic ;  Andrew Zisserman http://ieeexplore.ieee.org/document/4270197/

# TODO

[ ] Add post-processed version including QE, and diffusion. 
[ ] Add INSTRE dataset. 
