# Each model tested with all 292 quarterbacks from the 2006-2022 NFL seasons.

## Game by game rush attempts non autoregressive
![scatter_rush_mae_non](https://github.com/user-attachments/assets/8e4131b4-650a-404c-8cb9-fd352efde8d9)
This scatter plot shows how accurate each model is at predicting quarterback performance by comparing their mean absolute errors (MAE). You can see that the Random Forest model generally performs better, staying consistently low across most QBs. The Linear Regression model has a few major outliers, which means it struggled with some players. Overall, the Random Forest model looks like the most reliable option out of the three.

![rush_box_rush_mae_non](https://github.com/user-attachments/assets/cf25b3ac-c2d1-423b-907f-02f227ee7051)
This box plot compares how each model performed in terms of prediction error. The Random Forest model has the lowest and most consistent errors, this shows it’s the most reliable option. Linear Regression has a wider spread and a few outliers, including one very extreme case near 70, which really skews its performance. The Dummy Model stays relatively steady but isn’t as accurate, highlights the strength of using more advanced methods like the Random Forest.

![rush_mae_hist_dummy_mae_non](https://github.com/user-attachments/assets/0297b5df-e57e-4ae5-90f8-89ae1abefe00)
This histogram shows how often different Mean Absolute Error values occurred for our Dummy Model. Most of the predictions had low error values, with the majority between 0 and 3. That said, there are a few predictions with much higher errors, which stretch the distribution slightly to the right. Overall, the Dummy Model is simple and consistent, but not the most accurate option.

![rush_mae_hist_linear_mae_non](https://github.com/user-attachments/assets/ce34a7d0-f9af-45d3-a558-e9232cc47eaa)
This histogram shows the Mean Absolute Error distribution for the Linear Regression model. Most of the predictions are at the lower end, between 0 and 3, which is a good sign overall. However, there are a few instances where the error jumps significantly sclose to 15 and beyond, which indicates the model struggles with certain outliers. While generally more accurate than a dummy model, Linear Regression clearly has moments where it makes errors.

![rush_mae_hist_rand_for_mae_non](https://github.com/user-attachments/assets/1671cccf-8fae-4c89-a286-c34e44f97c32)
This histogram shows the Mean Absolute Error distribution for the Random Forest model. Almost all the predictions are tightly packed between 0 and 3, with few predictions straying from that range. Compared to the other models, Random Forest shows the most consistent and accurate results, with very few large errors. It’s clear from this plot that Random Forest handled the predictions much better overall.

![rush_combined_mae_hist_non](https://github.com/user-attachments/assets/2f31bd9b-b546-456b-881f-2bac99090482)
This overlayed histogram gives a side by side look at how all three models performed. You can see that the Random Forest model (green) consistently has lower errors and stays packed tightly near zero. The Linear Regression model (red) has mostly low errors too but shows a few bigger mistakes, stretching out to the right. The Dummy Model (blue) is the least accurate overall, with a wider spread of errors compared to the smarter models.


## Game by game rush attempts autoregressive
![rush_scatter_mae_auto](https://github.com/user-attachments/assets/f2f26c90-fc3c-4205-92a9-b6206c770b15)
This scatter plot shows how well different models predicted game by game passing touchdowns for each quarterback without using previous game information (non-autoregressive). The Random Forest model (green) generally had the lowest prediction errors, staying tight across most QBs. The Linear Regression model (blue) had a few bigger misses, with some errors jumping above 5 touchdowns. Overall, Random Forest once again proved to be the most stable and accurate model for this task.

![rush_box_mae_auto](https://github.com/user-attachments/assets/d73dd82e-070e-4089-a1e0-add61f3607de)
This box plot compares the distribution of mean absolute error across the three models. Random Forest not only had the lowest median error but also the smallest spread, making it the most consistent performer. Linear Regression had slightly higher errors and a few big outliers that hurt its reliability. Meanwhile, the Dummy Model performed worse overall, with more frequent and larger errors compared to the other two.

![rush_hist_mae_dummy_auto](https://github.com/user-attachments/assets/dc6eef83-a760-4f9b-bc1f-44e23aaee43a)
This histogram shows the distribution of Mean Absolute Error for the Dummy Model. Most of the predictions had low errors between 0 and 3, but there’s still a noticeable tail with a few higher errors up to around 10. While the Dummy Model is simple and provides a baseline, it's clear that more advanced models consistently do better. Overall, the Dummy Model’s performance is decent for comparison but not ideal for real predictions.

![rush_hist_mae_linear_auto](https://github.com/user-attachments/assets/7f4a75b3-dbcb-4cf0-b3bd-b561ec7f5c43)
This histogram shows the distribution of Mean Absolute Error for the Linear Regression model. Most of the predictions fall within the 0 to 3 range, showing good overall performance. However, there are a few outliers with much larger errors, which highlight that Linear Regression occasionally struggles with certain cases. Even with some misses, it generally performs better than the Dummy Model.

![rush_hist_mae_rand_for_auto](https://github.com/user-attachments/assets/63e24dd2-5222-4890-bfd0-63fbf7cede1f)
This histogram of the Random Forest model's MAE shows a tight and impressive performance. Nearly all predictions fall below an error of 3, with most errors densely concentrated near 0. There are no extreme outliers, which highlights the model's consistency and robustness. Compared to the Dummy and Linear Regression models, Random Forest clearly delivers the most accurate and reliable results.

![rush_combined_mae_auto](https://github.com/user-attachments/assets/d2c7744c-68e2-40d7-b4ab-f74a3b9efedd)
This overlayed histogram clearly shows how the three models compare in terms of prediction accuracy. The Random Forest model (green) outperforms the others, with its MAE values tightly concentrated near zero. Linear Regression (red) also does reasonably well but has a few outliers with higher errors. The Dummy Model (blue), while providing a basic benchmark, shows more frequent and wider errors, highlighting the advantage of using smarter models like Random Forest.


## Game by game touchdowns non autoregressive
### Passing touchdowns
![pass_td_scatter_mae_non](https://github.com/user-attachments/assets/2634bf5b-811d-4d86-96fc-c29a16604889)
This scatter plot shows the quarterback's Mean Absolute Error distribution. In this case, Random Forest shows a tighter cluster for low errors while Linear Regression has larger outliers.

![pass_td_box_mae_non](https://github.com/user-attachments/assets/9f816f87-b20b-46a4-a838-650a42c45414)
This box plot compares the Mean Absolute Error Distrubutions for each of the models. Once again, the Random Forest model maintains low errors while Linear Regression and Dummy Models show more frequent errors.

![pass_td_hist_mae_dummy_non](https://github.com/user-attachments/assets/a83755c8-b9ec-4ace-b28b-6fd228e849f1)
This histogram shows the Dummy Models MAE distribution clusters. The results stay consistent between 0 and 2, but still remains wider than Random Forest.

![pass_td_hist_mae_linear_non](https://github.com/user-attachments/assets/f32b6e2c-fd0d-4c75-9b7c-b80915d9b8ea)
This histograms shows MAE distributions for Linear Regression. Errors seem to remain low. However, there is a tail that stretches right which may indicate that there are the occasional poor predictions when compared to the other models.

![pass_td_hist_mae_rand_for_non](https://github.com/user-attachments/assets/e321d72a-b0ec-46b8-99dc-417ba8f25139)
In this Histogram, predictions for Random Forest are tightly packed which would mean that there are almost no major outliers, supporting it's consistent and acurate predictions.

![pass_td_combined_hist_mae_non](https://github.com/user-attachments/assets/6c493982-c0d4-4816-b084-27d0eb22322b)
This combined histogram compares each of the models side by side to show all error distributions. Random Forest maintained an overall low error distribution, surpassing both the linear regression and dummy models.

### Rushing touchdowns
![rush_td_scatter_mae_non](https://github.com/user-attachments/assets/9b33bb01-2c1f-4d7b-8a51-02bd2c8edb67)
This scatter plot breaks down the Mean Absolute Error (MAE) for each quarterback across three models. The Random Forest model (green) consistently stays low and tightly grouped, showing strong, reliable performance across most QBs. Linear Regression (blue) occasionally spikes, showing it's more prone to outliers, while the Dummy Model (red) generally performs worse and shows more variation. Overall, this confirms that Random Forest delivers the most accurate and stable predictions in this non-autoregressive setup.

![rush_td_box_mae_non](https://github.com/user-attachments/assets/3129a7eb-817a-4730-bc75-d1fdc967f270)
This box plot compares the MAE distributions for each model and reinforces the earlier findings. The Random Forest model has the lowest median error and the smallest spread, showing consistent accuracy with minimal outliers. Linear Regression performs decently but includes several outliers, including one that spikes above 6, suggesting instability in some predictions. The Dummy Model remains the weakest, with a higher overall spread and more frequent larger errors.

![rush_td_mae_hist_dummy_non](https://github.com/user-attachments/assets/63910ba1-c31d-42e8-91da-a135c547ba7a)
This histogram for the Dummy Model shows an even clearer concentration of MAE values tightly packed near zero. While the frequency of low-error predictions is high, it’s important to note that this baseline model lacks the intelligence to adapt to individual quarterbacks or game conditions. Although it's consistent, it’s not particularly accurate compared to the smarter models. This reinforces the need for more advanced approaches like Random Forest or even Linear Regression when precision matters.

![rush_td_mae_hist_linear_non](https://github.com/user-attachments/assets/af1c554d-fde3-4b09-938f-5ecf6337edf9)
This histogram of the Linear Regression model shows that nearly all MAE values are tightly clustered close to zero, which is a good sign. However, there's a small tail indicating occasional larger errors, hinting that while the model is generally reliable, it can still misfire in some cases. It performs much better than the Dummy Model overall but still doesn’t match the consistency that we see in the Random Forest. The visual confirms Linear Regression is a solid option which is more advanced than a baseline, but not quite the best.

![rush_td_mae_hist_rand_for_non](https://github.com/user-attachments/assets/6e4c03f6-2bc4-4134-abad-f16bd81c7de6)
The histogram for the Random Forest model shows it’s doing a great job—most of the prediction errors are really small and packed close to zero. That means it’s not just accurate, but also super consistent across the board. Unlike the other models, there aren’t any big spikes or outliers, which makes it a really dependable choice. If you're picking a model based on performance, Random Forest is clearly the one you can count on.

![rush_td_combined_hist_mae_non](https://github.com/user-attachments/assets/cbb7f342-3ecc-4aa8-a098-9769a6752ac0)


### Total touchdowns
![total_td_scatter_mae_non](https://github.com/user-attachments/assets/5009e00b-23a7-456d-ac42-433cd638dbe8)

![total_td_box_mae_non](https://github.com/user-attachments/assets/2189a0b0-e484-4ed2-b219-580be548ba96)

![total_td_hist_mae_dummy_non](https://github.com/user-attachments/assets/09a933a4-8964-4b06-a4bf-6928d42806d7)

![total_td_hist_mae_linear_non](https://github.com/user-attachments/assets/035a0f67-fef2-4a41-897f-2b399b5e3142)

![total_td_hist_mae_rand_for_non](https://github.com/user-attachments/assets/2c733bc1-7a1d-4db8-8633-0720568aecf9)

![total_td_combined_mae_hist_non](https://github.com/user-attachments/assets/f9ba82d8-b7af-443c-adec-91188b4d70f8)


## Game by game touchdowns autoregressive
### Passing touchdowns

![pass_td_scatter_mae_auto](https://github.com/user-attachments/assets/b26b66ac-f7c9-4173-9bb0-272f1e0f950d)

![pass_td_box_mae_auto](https://github.com/user-attachments/assets/fafd4a9e-bdb2-4b5f-a866-d1ad95194810)

![pass_td_hist_dummy_auto](https://github.com/user-attachments/assets/1176f249-b7da-4f21-a78a-5e84103322fd)

![pass_td_hist_linear_auto](https://github.com/user-attachments/assets/6b23625f-cb1d-42bf-89f9-05c49bf9ea6b)

![pass_td_hist_rand_for_auto](https://github.com/user-attachments/assets/53e72abc-1567-48ba-96b5-4deb2eca2ef7)

![pass_td_combined_hist_auto](https://github.com/user-attachments/assets/f1057939-1515-434a-8d79-d284f621f93a)


### Rushing touchdowns
![rush_td_scatter_mae_auto](https://github.com/user-attachments/assets/6d95a12c-0648-404e-ad01-9ba45571fbf9)

![rush_td_box_mae_auto](https://github.com/user-attachments/assets/2a0463b6-6f21-442e-b953-aa30f30a187d)

![rush_td_hist_mae_dummy_auto](https://github.com/user-attachments/assets/bd19b9a2-fbd0-4cd9-9868-884bc42fcb84)

![rush_td_hist_mae_linear_auto](https://github.com/user-attachments/assets/d589b3f7-9007-42f2-8ed6-5817427d66f3)

![rush_td_hist_mae_rand_for_auto](https://github.com/user-attachments/assets/feb2cfe3-c895-44c1-8979-9994e3f33514)

![rush_td_combined_hist_mae_auto](https://github.com/user-attachments/assets/31074cb5-44fd-40d9-b709-a2b945c71532)


### Total touchdowns

![total_td_scatter_mae_auto](https://github.com/user-attachments/assets/8324babb-782c-479e-ba23-3c49245a1ac9)

![total_td_box_mae_auto](https://github.com/user-attachments/assets/e2244dcb-401c-42d7-97f1-757f49066e23)

![total_td_hist_dummy_mae_auto](https://github.com/user-attachments/assets/8858dd97-a387-48ae-a795-78348accdd1e)

![total_td_hist_linear_mae_auto](https://github.com/user-attachments/assets/1bbfa29b-32ae-4c61-bb88-5df82626cbec)

![total_td_hist_rand_for_mae_auto](https://github.com/user-attachments/assets/6e078fa7-195b-46d7-b035-bede7f9d0d9b)

![total_td_combined_hist_mae_auto](https://github.com/user-attachments/assets/b557e441-ab11-45c7-82cb-df4d0740e722)




















