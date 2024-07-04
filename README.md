# Osun State Election

Introduction:

In this analysis, I worked on recent Osun State election result, to uncover hidden patterns, insights in the voting abnormalities of the results by comparing the votes each party received in a polling unit to the neighbouring units votes.

Methodology:

Data Loading & Preparation:

After loading the dataset, I retrieved the geographical coordinates (Latitude and Longitude) of each polling unit/ward. This was done by using OpenCage Geocoding Api to pinpoint accurately each polling unit/ward by using some features in the dataset like Local Government Area, Ward and State. This was able to help us identify the locations where the election took place.

The Neighbours column is a list of neighbouring poling units within a distance of 1km. They are represented by their index number of the dataset.

IDENTIFYING OUTLIERS USING Z-SCORES:

To identify the outliers for each party(APC, LP, PDP, NNPP), we calculated the outlier scores to identify the Outlier polling units where the voting results deviate significantly from neighbouring units. We calculated the mean and standard deviation of the votes among its neighbouring units. The Z-score measures how many standard deviations an observation is from the mean.

SORTED AND REPORTING:

We sorted the data by the outlier scores for each party in descending order which helped us to identify most significant outliers.

SUMMARY OF FINDINGS:

After calculating the outliers, we sorted the dataset by the outlier scores for each party in a descending order

TOP 3 OUTLIERS:
These are the top 3 outliers identified in each political parties along with their outlier score:

APC:

BORIPE, COLLEGE/EGBADA ROAD, OSUN:
Outlier Score : 4.25
Location: (7.5, 4.5)
Explanation:
a.) With an outlier score of 4.25, the APC vote count at BORIPE, COLLEGE/EGBADA ROAD, OSUN is extremely unusual compared to neighbouring polling units.
b.) There could be a strong local support for APC in this area.
IFE EAST, MODAKEKE III, OSUN:
Outlier Score: 3.71
Location: (7.5, 4.5)
Explanation:
a.) The APC vote at IFE EAST, MODAKEKE III, OSUN is also unusual compared to its neighbouring polling units.
b.) Intensive campaigning or lack thereof by the APC in this area could result in a substantial difference in the vote count.
EDE NORTH, OLOGUN/AGBAAKIN, OSUN:
Outlier Score : 3.61
Location: (7.5, 4.5)
Explanation:
a.) With an outlier score of 3.61, the APC vote count at EDE NORTH, OLOGUN/AGBAAKIN, OSUN is unusual compared to neighbouring polling units.
b.) Specific conditions on the election day such as weather or incidents at the polling unit might have influenced voter behaviour.

![APC_Outlier](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/f32d5457-a2ba-445e-a801-513955d8ac3f)
![Screenshot 2024-07-04 at 10 16 39 PM](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/84c60051-b7ef-49de-9bef-1069b89947ea)

PDP:

EDE NORTH, ALUSEKERE, OSUN:
Outlier Score: 5.39
Location : (7.7727, 4.5587)
Explanation:
Factors such as local leadership, campaign strategies, or demographic factors may contribute to its outlier status.
EDE SOUTH, ALAJUE I, OSUN:
Outlier Score: 4.45
Location: (7.7628, 4.5569)
Explanation:
Possible reasons for its outlier status include unique local issues, candidate popularity, or demographic characteristics impacting voting.
ILA, ISEDO I, OSUN:
Outlier Score: 11.52
Location: (7.733125, 4.515179)
Explanation:
Its outlier status could stem from varying community dynamics, campaign strategies, or demographic factors compared to neighboring units.

![PDP_Outlier](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/b2eff261-b8dc-44a0-9bf8-3132abe88304)
![Screenshot 2024-07-04 at 10 17 52 PM](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/0dabc1e8-a792-45d9-ada8-a2855f17c1ac)


LP:

EJIGBO, ELEJIGBO ‘C’/MAPO, OSUN:
Outlier Score: 73.59
Location: (7.90292, 4.31419)
EXPLANATION:
Possible reasons for its outlier status include specific local issues, candidate appeal, or demographic characteristics not shared by neighboring units.
ATAKUMOSA EAST, IWARA, OSUN:
Outlier Score: 21.398
Location: (7.5333, 4.7167)
EXPLANATION:
Its outlier status could be due to unique community issues, candidate support, or demographic factors affecting voter decisions.
ATAKUMOSA EAST, IGANGAN, OSUN:
Outlier Score: 14.679
Location: (7.3833, 4.7333)
EXPLANATION:
Specific conditions on the election day such as weather or incidents at the polling unit might have influenced voter behaviour.

![LP_OUTLIER](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/855bcab9-0736-41e3-b000-557ce4ad77a8)
![Screenshot 2024-07-04 at 10 18 45 PM](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/4df3ce96-aee2-4ce3-acd1-2baac79eb3dc)


NNPP:

EDE SOUTH, ALAJUE I, OSUN:
Outlier Score: 50.879
Location: (7.7000, 4.4500)
EXPLANATION:
Its outlier status could be due to unique community issues, candidate support, or demographic factors affecting voter decisions.
EDE NORTH, SABO/AGBONGBE II, OSUN:
Outlier Score: 23.21
Location: (7.7411, 4.4510)
EXPLANATION:
Specific conditions on the election day such as weather or incidents at the polling unit might have influenced voter behaviour.
ILA, ISEDO I, OSUN:
Outlier Score: 18.61
Location: (8.019116, 4.901962)
EXPLANATION:
Possible reasons for its outlier status include specific local issues, candidate appeal, or demographic characteristics not shared by neighboring units.

![NNPP_Outlier](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/e9f6a31d-82bb-4189-b3dc-1949904edbb2)
![Screenshot 2024-07-04 at 10 19 33 PM](https://github.com/Raphlawren/Osun_State_Election/assets/130583230/efa6410e-8a50-41de-9ff2-d7b0ef194781)

CONCLUSION:
The analysis shows that the four political parties had some outliers in various polling unit.


The dataset can be accessed [here](https://docs.google.com/spreadsheets/d/1_DEH5sEsZsFS8z5qHcGX_C5RhK0aghNa/edit?gid=663511907#gid=663511907)
