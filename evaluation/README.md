# EVALUATING THE SOTA MODELS

we validate the effectiveness and efficiency of state-of-the-art multimodal recommendation models by conducting extensive experiments on four public datasets. Furthermore, we investigate the principal determinants of model performance, including the impact of different modality information and data split methods.

## Statistics of the evaluated datasets.
| Datasets | # Users | # Items | # Interactions |Sparsity|
|----------|--------|---------|---------|---------|
| Baby     | 19,445     | 7,050     |160,792|99.8827%|
| Sports   | 35,598      | 18,357   |296,337|99.9547%|
| FoodRec     | 61,668      | 21,874    |1,654,456|99.8774%|
| Elec     | 192,403      | 63,001     |1,689,188|99.9861%|


## Experimental Results
| Dataset                 | Model    | Recall@10          | Recall@20          | Recall@50          | NDCG@10            | NDCG@20            | NDCG@50            |
|-------------------------|----------|--------------------|--------------------|--------------------|--------------------|--------------------|--------------------|
| **Baby**   | BPR      | 0.0357             | 0.0575             | 0.1054             | 0.0192             | 0.0249             | 0.0345             |
|                         | LightGCN | 0.0479             | 0.0754             | 0.1333             | 0.0257             | 0.0328             | 0.0445             |
|                         | VBPR     | 0.0423             | 0.0663             | 0.1212             | 0.0223             | 0.0284             | 0.0396             |
|                         | MMGCN    | 0.0378             | 0.0615             | 0.1100             | 0.0200             | 0.0261             | 0.0359             |
|                         | DualGNN  | 0.0448             | 0.0716             | 0.1288             | 0.0240             | 0.0309             | 0.0424             |
|                         | GRCN     | 0.0539             | 0.0833             | 0.1464             | 0.0288             | 0.0363             | 0.0490             |
|                         | LATTICE  | 0.0547             | 0.0850             | 0.1477             | 0.0292             | 0.0370             | 0.0497             |
|                         | BM3      | 0.0564             | 0.0883             | 0.1477             | 0.0301             | 0.0383             | 0.0502             |
|                         | SLMRec   | 0.0529             | 0.0775             | 0.1252             | 0.0290             | 0.0353             | 0.0450             |
|                         | ADDVAE   | _0.0598_ | _0.091_  | _0.1508_ | _0.0323_ | _0.0404_ | _0.0525_ |
|                         | FREEDOM  | **0.0627**    | **0.0992**    | **0.1655**    | **0.0330**    | **0.0424**    | **0.0558**    |
| **Sports**  | BPR      | 0.0432             | 0.0653             | 0.1083             | 0.0241             | 0.0298             | 0.0385             |
|                         | LightGCN | 0.0569             | 0.0864             | 0.1414             | 0.0311             | 0.0387             | 0.0498             |
|                         | VBPR     | 0.0558             | 0.0856             | 0.1391             | 0.0307             | 0.0384             | 0.0492             |
|                         | MMGCN    | 0.0370             | 0.0605             | 0.1078             | 0.0193             | 0.0254             | 0.0350             |
|                         | DualGNN  | 0.0568             | 0.0859             | 0.1392             | 0.0310             | 0.0385             | 0.0493             |
|                         | GRCN     | 0.0598             | 0.0915             | 0.1509             | 0.0332             | 0.0414             | 0.0535             |
|                         | LATTICE  | 0.0620             | 0.0953             | 0.1561             | 0.0335             | 0.0421             | 0.0544             |
|                         | BM3      | 0.0656             | 0.0980             | 0.1581             | 0.0355             | 0.0438             | 0.0561             |
|                         | SLMRec   | 0.0663             | 0.0990             | 0.1543             | 0.0365             | 0.0450             | 0.0562             |
|                         | ADDVAE   | _0.0709_ | _0.1035_ | _0.1663_ | _0.0389_    | _0.0473_ | _0.0600_ |
|                         | FREEDOM  | **0.0717**    | **0.1089**    | **0.1768**    | **0.0385** | **0.0481**    | **0.0618**    |
| **FoodRec** | BPR      | 0.0303             | 0.0511             | 0.0948             | 0.0188             | 0.0250             | 0.0356             |
|                         | LightGCN | 0.0331             | 0.0546             | 0.1003             | 0.0210             | 0.0274             | 0.0386             |
|                         | VBPR     | 0.0306             | 0.0516             | 0.0972             | 0.0191             | 0.0254             | 0.0365             |
|                         | MMGCN    | 0.0307             | 0.0510             | 0.0943             | 0.0192             | 0.0253             | 0.0359             |
|                         | DualGNN  | _0.0338_ | 0.0559             | _0.1027_ | _0.0214_ | _0.0280_ | _0.0394_ |
|                         | GRCN     | **0.0356**   | **0.0578**    | **0.1063**    | **0.0226**    | **0.0295**    | **0.0411**    |
|                         | LATTICE  | 0.0336             | _0.0560_| 0.1012             | 0.0211             | 0.0277             | 0.0388             |
|                         | BM3      | 0.0334             | 0.0553             | 0.0994             | 0.0208             | 0.0274             | 0.0381             |
|                         | SLMRec   | 0.0323             | 0.0515             | 0.0907             | 0.0208             | 0.0266             | 0.0362             |
|                         | ADDVAE   | 0.0309             | 0.0508             | 0.093              | 0.0186             | 0.0247             | 0.035              |
|                         | FREEDOM  | 0.0333             | 0.0556             | 0.1009             | 0.0212             | 0.0279             | 0.0389             |
| **Elec**    | BPR      | 0.0235             | 0.0367             | 0.0621             | 0.0127             | 0.0161             | 0.0212             |
|                         | LightGCN | 0.0363             | 0.0540             | 0.0879             | 0.0204             | 0.0250             | 0.0318             |
|                         | VBPR     | 0.0293             | 0.0458             | 0.0778             | 0.0159             | 0.0202             | 0.0267             |
|                         | MMGCN    | 0.0213             | 0.0343             | 0.0610             | 0.0112             | 0.0146             | 0.0200             |
|                         | DualGNN  | 0.0365             | 0.0542             | 0.0875             | 0.0206             | 0.0252             | 0.0319             |
|                         | GRCN     | 0.0389             | 0.0590             | 0.0970             | 0.0216             | 0.0268             | 0.0345             |
|                         | LATTICE  | -                  | -                  | -                  | -                  | -                  | -                  |
|                         | BM3      | 0.0437             | 0.0648             | 0.1021             | 0.0247             | 0.0302             | 0.0378             |
|                         | SLMRec   | _0.0443_ | _0.0651_ | _0.1038_ | _0.0249_ | _0.0303_ | _0.0382_ |
|                         | ADDVAE   | **0.0451**    | **0.0665**    | **0.1066**    | **0.0253**    | **0.0308**    | **0.0390**    |
|                         | FREEDOM  | 0.0396             | 0.0601             | 0.0998             | 0.0220             | 0.0273             | 0.0353             |



## Please consider to cite our paper if this model helps you, thanks:
```
@article{zhou2023comprehensive,
  title={A Comprehensive Survey on Multimodal Recommender Systems: Taxonomy, Evaluation, and Future Directions},
  author={Zhou, Hongyu and Zhou, Xin and Zeng, Zhiwei and Zhang, Lingzi and Shen, Zhiqi},
  journal={arXiv preprint arXiv:2302.04473},
  year={2023}
}