---
layout: single
title: 
permalink: /Projects/
date: 2023-9-02
categories: pages
toc: false
toc_label: "Projects"
toc_icon: "columns"
---
<style>
    body {
        color: #333; /* Default text color */
    }
    
    .project-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    
    .project {
        width: 100%; /* Full width */
        box-sizing: border-box; */
        padding: 20px; */
        border: 1px solid #ccc; */
        margin-top: 20px; /* Add space between projects */
    }

    .project h2 {
        margin-top: 0;
    }

    .project img {
        max-width: 100%;
        height: auto;
    }

    /* Style for legend on the left */
    .legend {
        float: top;
        width: 50%; /* Adjust the width as needed */
        padding-right: 20px; Add space between legend and projects */
    }

    .legend ul {
        list-style: none;
        padding: 0;
    }

    .legend li {
        /* margin: 15px 0; */ */
        font-size: 17px; /* Adjust the font size for the legend */
    }

    /* Style for the title */
    h1 {
        color:  #336699; /* Change the title text color to blue */
    }
</style>
<!-- Title of the page in blue -->
<h1>Projects</h1>
<br>
<!-- Legend on the top -->
<div class="legend" style="font-size: 18px;">
    <ul>
        <li><a href="#project1" style="text-decoration: none;">🌿 Identifying Leaf Phenology</a></li>
        <li><a href="#project2" style="text-decoration: none;">🚗 Uber Data Analytics</a></li>
        <li><a href="#project3" style="text-decoration: none;">💳 Credit Card Fraud Detection</a></li>
        <li><a href="#project4" style="text-decoration: none;">💰 Salary Prediction</a></li>
        <li><a href="#project5" style="text-decoration: none;">📷 Image Classifier Using CNN</a></li>
    </ul>
</div>
<br>
<div class="project-container">
    <div id="project1" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>IDENTIFYING LEAF PHENOLOGY OF DECIDUOUS BROADLEAF FORESTS FROM PHENOCAM IMAGES</strong></h2>
        <p><i>In Progress</i></p>
        <div class="image-container" style= "align-items: center;" ><img src="/assets/images/decidousForest.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
           The ongoing project undertaken by the individual showcases pioneering efforts in advancing phenological research through the integration of state-of-the-art technology and deep learning techniques. The focus lies on predictive modeling and large-scale validation, with the goal of revealing the intricate correlations between PhenoCam images and the development of vegetation phenology <br>
           At its essence, the project revolves around the creation of a predictive tool employing CNN Regression to anticipate leaf phenology in deciduous broadleaf forests across diverse sites. The project employs three primary methods - AlexNet, ResNet-50, and ResNet-101 - each contributing distinctively to the comprehension of phenology patterns. By harnessing the capabilities of deep learning, the project seeks to unearth nuanced insights from PhenoCam images, potentially uncovering subtleties that evade human observation.<br>
        </p>
        <a href="https://github.com/AmritaNeogi/PhenoCam-Image-Analysis-Using-CNN" style="text-decoration: none;">Know More </a><img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"> <br><br>
    </div>
       <div id="project2" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>UBER DATA ANALYTICS</strong></h2>
        <p><i>August 2023</i></p>
        <div class="image-container"><img src="/assets/images/uber-header.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
            Executed a comprehensive end-to-end data engineering project leveraging a real-world Uber dataset to demonstrate my expertise in data handling and analysis. Employed Google Cloud Storage to efficiently manage data extraction and transformation processes. Successfully processed and loaded data using Mage ETL, achieving an impressive average extraction rate of 500 records per second. 
            <a class="image-container"><img src="/assets/images/Overview.png" alt="Project Image"></a><br>
            <!-- <a class="image-container"><img src="/assets/images/uber_data_model.jpeg" alt="Project Image"></a><br> -->
            Performed complex analytical queries on the enriched dataset using BigQuery, showcasing my ability to derive meaningful insights from vast datasets. Developed and optimized queries that consistently yielded results within seconds, contributing to efficient data-driven decision-making. Answered crucial business questions, such as demand patterns and peak hours, enhancing my analytical capabilities.<br>
            Implemented an interactive and intuitive Looker dashboard that translated raw data into actionable visualizations. The dashboard facilitated dynamic exploration of key performance indicators, resulting in a 30% increase in data accessibility for stakeholders. This project not only strengthened my technical skills but also highlighted my proficiency in creating user-friendly data representation tools.<br>
            <a href= "https://lookerstudio.google.com/s/s-nnQQB79Kw" style="text-decoration: none;">Looker Dashboard</a> <br>
            <a class="image-container"><img src="/assets/images/uber_dashboard.jpg" alt="Project Image"></a><br> 
        </p>
        <a href="https://github.com/AmritaNeogi/Uber_data_Analytics" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"><br><br>
    </div>
    <div id="project3" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>CREDIT CARD FRAUD DETECTION</strong></h2>
        <p><i>August 2023</i></p>
        <div class="image-container" style= "align-items: center;" ><img src="/assets/images/credit_card.jpeg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
            In the realm of digital transactions, security is paramount. My project focuses on creating a robust credit card fraud detection model using advanced machine learning algorithms. <br> 
            The standout model boasts an accuracy rate that sets a new standard for fraud detection.Machine learning algorithm such as Decision Tree, Logistic Regression, Random Forest and Naive Bayes, have been employed, and obtained an impressive accuracy rate of 99% for the best model. 
            Later, the data imbalance was tackled using SMOTE Technique. Each algorithm was fine-tuned for optimal performance and further acheieved a 10% increase in the accuracy.<br>
            <a class="image-container"><img src="/assets/images/final_summary.png" alt="Project Image"></a><br> 
        </p>
        <a href="https://github.com/AmritaNeogi/Data-Science-Project-Credit-Card-Fraud-Detection" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"><br><br>
    </div>
       <div id="project4" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>SALARY PREDICTION</strong></h2>
        <p><i>July 2023</i></p>
        <div class="image-container"><img src="/assets/images/salary_pred.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
           The objective of this project is to construct a model for salary prediction contingent on years of experience.<br>
           Through meticulous refinement and adept utilization of the Gradient Descent technique, an exceptionally efficient model was constructed. The core of the accomplishment rests in the notable decrease of the Mean Square Error (MSE). The model rapidly reduced the MSE from a substantial 91.2% to an impressive 6.3%.<br>
        </p>
        <a href="https://github.com/AmritaNeogi/Data-Science-Project-Salary-Prediction" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"> <br><br>
    </div>
      <div id="project5" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>DESIGN AND IMPLEMENTATION OF AN IMAGE CLASSIFIER USING CNN</strong></h2>
        <p><i>December 2022</i></p>
        <div class="image-container"><img src="/assets/images/image_classifier.png" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
            In the realm of cutting-edge technology, the project embarked on a journey of unraveling the potential of deep convolution networks for largescale image classification. Demonstrating precision, the project culminated in an impressive accuracy rate of 91.21%. <br>
            Employing a sophisticated arsenal of Python libraries, including NumPy, Pandas, and PyTorch, the project navigated the complex landscape of image classification.<br>
        </p>
        <a href="https://github.com/ISTA421INFO521/final-project-AmritaNeogi" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;">
    </div>  
</div>
