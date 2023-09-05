# Quantitative Soil Analysis using Vis-NIR Spectra
1. Various models have been applied to predict soil properties from Vis-NIR spectra. Some models have shown good performance with specific properties, and poor performance with others. Some machine learning models that have been used are PLSR, RF, cubist, multivariate adaptive regression spline (MARS).

2. Several deep learning models have also been used including artificial neural networks (ANN) and convolutional neural networks (CNN).

3. The different metrics used to evaluate the developed models are coefficient of determination (𝑅𝑅2 ), Relative Percentage Difference (RPD), Root Mean Squared Error (RMSE), and Standard Error of Prediction (SEP).

4. These are the graphs showing the evolution of Loss and R^2 over epochs
   
4.1. ![image](https://github.com/h2ars/Soil_quantitative/assets/72066376/f40f1d97-b1b4-459d-b7bf-fc107b1fefc7)

6. VIS-NIR data from ~3600 soil samples have been used for training 8 soil properties- Ca, Na, Mg, K, C, 𝑝𝑝𝐻𝐻𝐻𝐻2𝑂𝑂, 𝑝𝑝𝐻𝐻𝐾𝐾𝐾𝐾𝐾𝐾 and Clay. The data used comes from ICRAF-ISRIC Soil VNIR Spectral Dataset. Random Forest, PLSR, XGBoost and MLP were used for prediction. Data was processed using SG Smoothening. Figure 2 and Figure 3 shows the raw data and processed data respectively. Both processed and unprocessed data was experimented with for training. The models were tried in both multi-output mode to predict all features together and in single output mode where separate models were trained for each output feature.

7. Original Data -
   
![image](https://github.com/h2ars/Soil_quantitative/assets/72066376/5ef8478d-8a5f-4a33-a027-745ee1662401)

8. Processed data (SG Smoothing) -
   
![image](https://github.com/h2ars/Soil_quantitative/assets/72066376/cf87505f-c551-49ad-bdef-38742f3663bd)

10. The purpose of this paper was to explore and implement dry methods which are unconventional from the wet (chemical) methods. After the pre-processing and smoothing of the dataset, XGBoost multilayer output (MO) outputs the maximum R2 value for maximum features. The best performance was from XGBoost trained on data processed using SG Smoothening in multioutput mode. Ca, Mg, C, 𝑝𝑝𝐻𝐻𝐻𝐻2𝑂𝑂 , 𝑝𝑝𝐻𝐻𝐾𝐾𝐾𝐾𝐾𝐾 , and Clay were predicted with good performance with 𝑅𝑅2 from 0.69 to 0.81.
11. The detailed comparison of the model performances are mentioned in Table.
    
![image](https://github.com/h2ars/Soil_quantitative/assets/72066376/f0ee314d-06e2-4a69-926b-5ff203b93b6c)

10. The research paper on this project has also been published in SMARTGEN CON, 2022 (IEEE Digital Xplore - https://ieeexplore.ieee.org/document/10084118)
