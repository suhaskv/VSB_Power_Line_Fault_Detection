# VSB Power Line Fault Detection

## Business Problem

Medium voltage overhead power lines run for hundreds of miles to supply power to cities. These great distances make it expensive to manually inspect the lines for damage that doesn't immediately lead to a power outage, such as a tree branch hitting the line or a flaw in the insulator. These modes of damage lead to a phenomenon known as partial discharge — an electrical discharge which does not bridge the electrodes between an insulation system completely. Partial discharges slowly damage the power line, so left unrepaired they will eventually lead to a power outage or start a fire.

The challenge here is to detect partial discharge patterns in signals acquired from these power lines with a new meter designed at the ENET Centre at VŠB. Effective classifiers using this data will make it possible to continuously monitor power lines for faults.

ENET Centre researches and develops renewable energy resources with the goal of reducing or eliminating harmful environmental impacts. Their efforts focus on developing technology solutions around transportation and processing of energy raw materials.

By developing a solution to detect partial discharge maintenance costs will be reduced, and power outages will be prevented.

Source: https://www.kaggle.com/c/vsb-power-line-fault-detection/overview

## Business Objectives and Constraints
1. Need to predict the PD-pattern very accurately with high Mathew Correlation Coefficient (MCC) value
2. Cost of failure to detect the PD-pattern is very severe as it might start a fire or affect livelihood of many because of power outage
3. No strict latency constraints. The models can take a few seconds, upto a minute to give the output.

## Machine Learning Problem Statement
The objective is to detect the Partial Discharge (PD) pattern present in the 3-phase AC medium voltage signal.

* If PD-pattern present in the signal - classified as 1
* If PD-pattern not present in the signal - classified as 0

Therefore, this is a Binary Classification Problem.

## Performance Metric
Matthews Correlation Coefficient (MCC) is used as the performance metric.

MCC measures the correlation between the predicted and the actual values of the output. MCC values range from -1 to 1.

* If MCC=-1: Predicted and Actual values are highly uncorrelated and are in complete disagreement.
* If MCC=1: Predicted and Actual values are highly correlated and are in complete agreement.
* If MCC=0: Correlation is equivalent to random prediction.

Source: https://www.kaggle.com/c/vsb-power-line-fault-detection/overview/evaluation

## References
* S. Misák, J. Fulnecek, T. Vantuch, T. Buriánek and T. Jezowicz, "A complex classification approach of partial discharges from covered conductors in real environment," in IEEE Transactions on Dielectrics and Electrical Insulation, vol. 24, no. 2, pp. 1097-1104, April 2017, doi: 10.1109/TDEI.2017.006135.
* [Analysis of Time Series Data](http://dspace.vsb.cz/bitstream/handle/10084/133114/VAN431_FEI_P1807_1801V001_2018.pdf)
* [1st place solution](https://www.kaggle.com/mark4h/vsb-1st-place-solution)
* [2nd place solution](https://www.kaggle.com/c/vsb-power-line-fault-detection/discussion/86616)
* [Discrete Wavelet Transform](https://www.kaggle.com/jackvial/dwt-signal-denoising)
* [Stacked Attention Bi-LSTM](https://www.kaggle.com/tarunpaparaju/vsb-competition-attention-bilstm-with-features?scriptVersionId=10690570)

