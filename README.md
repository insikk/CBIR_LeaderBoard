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
<td>[GeM]</td>
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
<td>[GeM]</td>
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
<td>[DeepIR]</td>
<td>&nbsp;</td>
</tr>

<td>BoW(200k)+VV</td>
<td>80.1</td>
<td>73.4</td>
<td>74.5</td>
<td>64.9</td>
<td>-</td>
<td>16.xx</td>
<td>[VV]</td>
<td>&nbsp;</td>
</tr>

<td>BoW(200k)</td>
<td>76.2</td>
<td>71.2</td>
<td>66.4</td>
<td>60.2</td>
<td>-</td>
<td>16.xx</td>
<td>[VV]</td>
<td>&nbsp;</td>
</tr>

<td>BoW(1M)+FSM</td>
<td>66.4</td>
<td>-</td>
<td>54.1</td>
<td>-</td>
<td>-</td>
<td>07.xx</td>
<td>[FSM]</td>
<td>&nbsp;</td>
</tr>


<td>BoW(1M)</td>
<td>61.8</td>
<td>-</td>
<td>49.0</td>
<td>-</td>
<td>-</td>
<td>07.xx</td>
<td>[FSM]</td>
<td>&nbsp;</td>
</tr>

</tbody>
</table>

* This result does not use Query Expansion (QE), Database Augmentation (DBA), or Spatial Verification.
* For BoW based Image Retrieval System, Spatial Verifiaction is necessary to consider spatial information. So, I explicitly add the spatial verification method after `+` symbol. (i.e FSM, VV)


[GeM]: Fine-tuning CNN Image Retrieval with No Human Annotation by Filip Radenović, Giorgos Tolias, Ondřej Chum https://arxiv.org/abs/1711.02512, 

[DeepIR]: End-to-end Learning of Deep Visual Representations for Image Retrieval
 by Albert Gordo, Jon Almazan, Jerome Revaud, Diane Larlus https://arxiv.org/abs/1610.07940

[FSM]: Object retrieval with large vocabularies and fast spatial matching by  James Philbin ;  Ondrej Chum ;  Michael Isard ;  Josef Sivic ;  Andrew Zisserman http://ieeexplore.ieee.org/document/4270197/

[VV]: A Vote-and-Verify Strategy for Fast Spatial Verification in Image Retrieval by Sch\"{o}nberger, Johannes Lutz and Price, True and Sattler, Torsten and Frahm, Jan-Michael and Pollefeys, Marc https://github.com/vote-and-verify/vote-and-verify
