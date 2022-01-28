---
title: Indoor Odometry and Point Cloud Mapping
date: '2017-12-01'
authors:
  - Prabhat Sanu Ligal
  - Bikram Acharya
  - admin
  - Prasun Shrestha
  - Pratik Pokharel
  - Sharad Kumar Ghimire
publication_types:
  - '1'
publication: 'In *Proceedings of IOE Graduate Conference*. '
publication_short: In *ICOEGC*
abstract: 
  Indoor localization and mapping is an important problem with many applications such as emergency response, architectural modeling, and historical preservation. In this project, a metrically accurate, GPS-denied, indoor 3D static mapping system was developed using a moveable base coupled with three degree of freedom IMU. The experiment was performed by scanning a flat apartment which closely resembled the actual test environment. First the distance of various elements in the surrounding was collected using the LiDAR module along with the orientation of LiDAR Lite. This is termed as scanning mode of the system. After full scan of an area, the system was manually switched to Odometry mode wherein the system was moved to another location for new scan. The distance travelled as well as the direction of travel was noted. Secondly, the data is processed to obtain the position of different points in 3D space. The vast data set is stored in Point Cloud format. The point cloud is processed and stitched by removing the outliers, clustering error-free data and segmenting data to different planes. The scanning and odometry are two different modes that are better operated separately. This is due to the fact that scanning takes time and simultaneous movement registered erroneous data. This increased the number of outliers and hence produced an anomalous map. The toggle between two modes are maintained using a manual switch which provided more accurate data on separate implementation.
summary: Indoor localization and mapping is an important problem with many applications such as emergency response, architectural modeling, and historical preservation. In this project, a metrically accurate, GPS-denied, indoor 3D static mapping system was developed using a moveable base coupled with three degree of freedom IMU.
image_preview: indoor.png
selected: true
projects: []
url_pdf: pdf/IOEGC-2017-28.pdf
url_preprint: ''
url_code: ''
url_dataset: ''
url_project: ''
url_slides: ''
url_video: ''
url_poster: ''
url_source: ''
math: true
highlight: true
header:
  image: indoor.png
  caption: Top view of Odometry Output for a floorplan

---