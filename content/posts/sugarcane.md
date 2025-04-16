+++
title = "Predicting Crop Yields from Satellite imagery"
description = "Overview of how we used Sentinel 2 satellite data to predict sugar cane yields"
tags = []
categories = []
+++

Using Machine Learning, we developed a method to predict sugar cane crop yields in Brazil for the 13 different processing mills days before the bi-weekly official crop yield report.

<!--more-->

#### Project Objectives:


{{< embed-pdf url="./AgriculturalFundProjectPDF.pdf"  >}}



#### What/How:

Below see how we are analyzing the outputs -- the NDVI shows the diff we see between multiple dates -- which can indicate crop harvest. To get this, we have to align images, do the NDVI calculation (non-trivial), determine the area, and then use historical crop yield actuals to determine what we think this area represents in terms of yield AND THEN build a model so we can look at other harvested areas and predict what the yield is like to be. Here we are looking at < 20 square miles -- but we are doing this on the order of 13,000 square km. Trickiest part? Cloud coverage.

#### Example output:

{{< embed-pdf url="./Agriculture-analysisPDF.pdf"  >}}


