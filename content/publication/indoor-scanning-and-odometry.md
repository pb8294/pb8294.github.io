+++
title = "Indoor Odometry and Point Cloud Mapping"

# Date first published.
date = "2017-12-01"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Prabhat Sanu Ligal", "Bikram Acharya", "Pradeep Bajracharya", "Prasun Shrestha", "Pratik Pokharel", "Sharad Kumar Ghimire"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "In *Proceedings of IOE Graduate Conference*. "
publication_short = "In *ICOEGC*"

# Abstract and optional shortened version.
abstract = "Indoor localization and mapping is an important problem with many applications such as emergency response, architectural modeling, and historical preservation. In this project, a metrically accurate, GPS-denied, indoor 3D static mapping system was developed using a moveable base coupled with three degree of freedom IMU. The experiment was performed by scanning a flat apartment which closely resembled the actual test environment. First the distance of various elements in the surrounding was collected using the LiDAR module along with the orientation of LiDAR Lite. This is termed as scanning mode of the system. After full scan of an area, the system was manually switched to Odometry mode wherein the system was moved to another location for new scan. The distance travelled as well as the direction of travel was noted. Secondly, the data is processed to obtain the position of different points in 3D space. The vast data set is stored in Point Cloud format. The point cloud is processed and stitched by removing the outliers, clustering error-free data and segmenting data to different planes. The scanning and odometry are two different modes that are better operated separately. This is due to the fact that scanning takes time and simultaneous movement registered erroneous data. This increased the number of outliers and hence produced an anomalous map. The toggle between two modes are maintained using a manual switch which provided more accurate data on separate implementation."
abstract_short = "A short version of the abstract."

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Links (optional).
url_pdf = "pdf/IOEGC-2017-28.pdf"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "headers/bubbles-wide.jpg"
caption = "My caption 😄"

+++