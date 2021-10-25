# Favour Umeh Portfolio
This portfolio highlights some of the projects that I have undergone in 2021. They are mostly data projects except for project 4 which is an automation project centred on Structural Engineering. 

## Project 1 (Data Engineering): [Basketball Reference Data Pipeline](https://github.com/favourumeh/DATA-PIPELINE)
- Created a data pipeline that can scrape and clean tabular statistical data from the basketball-reference [website](https://www.basketball-reference.com) and store it in a local MySQL server and/or Excel workbook. 
- The data in question is per-game statistics from the national Basketball Association (NBA) and it will be used to undergo regression and classifcation projects (see projects 2 and 3)
- The NBA is the top professional basketball league in North America. It was founded in 1947 and is currently home to the best basketball players in the world. 
- Before loading the data into CSV and MySQL a lot of cleaning and tranformative actions were undergone. The figure below shows the cleaning and transformative action undergone on the raw data
![](/Images/Cleaning_Actions.png)

## Project 2 (Data Science): [Identifying the position of an NBA player](https://github.com/favourumeh/Identifying-Player-Position)
 - Created a tool that enables an NBA scout to identify an NBA player's position based on their per 36minutes statistics using 6 classification models. 
 - Data for this project was taken from basketballreference.com using the pipeline tool developed in project (Project 1). 
 - This project uses three different classification algorithms: Naive Bayes, Logistic Regression and K Nearest Neighbours
 - In total six models were created:
    - three models used the individual algorithms mentioned above. They are called: 'KNN', 'log_reg' and 'GNB'
    - three more models were created using an ensemble approach. These ensemble models use hard voting with some minor tweaks which are explained in section 9. They are called: 'E_hv1', 'E_hv2' and 'E_hv_flex' 
 -  All models were evaluated by comparing each other against three classification metrics : precision, recall and accuracy. Their confusion matrices were also analysed to gauge how well each model performed for different labels (/classes). 
 -  Below are the confusion matrices for each model: 
![](/Images/Confusion_matrices_for_all_non-ensemble_models_for_evaluation_data.png)
![](/Images/Confusion_matrices_for_all_ensemble_models_for_evaluation_data.png)

## Project 3 (Data Science): [Predicting Turnovers](https://github.com/favourumeh/Multiple_Linear_Regression---Predicting-Turnovers-)
 - In this project two multiple linear regression models were created to predict the turnovers committed by an NBA player per 36 minutes (TOV)           
 - Ultimately it was found that Two-point attempts per36(2PA), Free throw Attempts per36(FTA) and Assists per36(AST) were the only factors from the dataset that had a notable effect on the TOV:
 
      - **R2 = 0.46** . This is low because the model does not factor a player's skill which is the primary predictor of TOV. The R2 suggests that there is a significant variance in skill level amongst players  
        
      - **RMSE = 0.529** . The value of this error is roughly 25% of the mean TOV observed. 

- The models created can be used to assists NBA coaches in player development because the model acts as a predictor of a player's expected TOV. A player vastly outperforming their expected TOV (i.e. commits less TOV than expected) could indicate good ball retention skills which would mean that they require more on-ball possessions. It can also be used to pinpoint players who need more training in ball retention. 
- The figure below shows displays the use of correlation plots for feature selection
![](/Images/Correlation_plot.png)


## Project 4 (Automation): [Automating the Design of Compression Members](https://github.com/favourumeh/compression_resistance)
- Created a tool that provides desk-based assessment of the adequacy of universal columns and beams (UKC and UKB) subjected to compressive loads. 
- It uses the following information on the beam and loading conditions:  
   - design compressive load applied on the member (in kN)
   - span of the member(in m)
   - young's modulus (in N/mm2 or MN/m2)
   - steel grade
   - member end connections (i.e. whether the member is pinned at both ends, fixed at both ends, pinned at one end (fixed at other end), etc)
   - nature of the loading on the web and flange(bending or compression) 

- This tool can be used by those with/without experience in Structural Engineering to perform quick design checks on the compression resistance of structural members
- The figure below show a universal beam
![](/Images/UKB_compressive_load_image.png)

Image reference: https://www.alcoengineering.co.uk/steel-universal-i-beams.html
