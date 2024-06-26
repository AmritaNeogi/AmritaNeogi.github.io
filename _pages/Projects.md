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
        <strong>Data Science & Machine Learning:</strong>
        <li><a href="#project1" style="text-decoration: none;">🌿 Identifying Leaf Phenology</a></li>
        <!-- <li><a href="#project9" style="text-decoration: none;">😷 Face Mask Detection</a></li> -->
        <li><a href="#project6" style="text-decoration: none;">🎀 Breast Cancer Prediction</a></li>
        <li><a href="#project3" style="text-decoration: none;">💳 Credit Card Fraud Detection</a></li>
        <li><a href="#project4" style="text-decoration: none;">💰 Salary Prediction</a></li>
        <li><a href="#project5" style="text-decoration: none;">📷 Image Classifier Using CNN</a></li>
        
        <strong>Data Engineering & Data Analytics:</strong>  
        <li><a href="#project8" style="text-decoration: none;">🏠 House Price Profiler using Snowflake Database</a></li>  
        <li><a href="#project7" style="text-decoration: none;">🎥 Youtube Data Pipeline using Apache Airflow</a></li>
        <li><a href="#project2" style="text-decoration: none;">🚗 Uber Data Analytics</a></li>  
            
    </ul>
</div>
<br>
<div class="project-container">
    <div id="project1" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>Phenophase Image Analysis</strong></h2>
        <p><i>December 2023</i></p>
        <div class="image-container" ><img src="/assets/images/decidousForest.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; align-items: center; font-size: 15px;">
           The intricate relationship between vegetation phenology and ecosystem functions shapes key ecological processes, influenced by climate-induced asynchrony. Phenological events, known as Phenophase, tie to seasonal transitions and precipitation. Consequences include disruptions like food scarcity and insect population growth. Despite predictive models, uncertainties persist in aligning Phenophase across species. <br>
           Leaf Growth and Dormancy phase for different years:
            <a class="image-container"><img src="/assets/images/SOS_EOS.png" alt="Project Image"></a><br>
            GAN Architechture:
             <a class="image-container"><img src="/assets/images/GAN.png" alt="Project Image"></a><br>
            To address this, tools like PhenoCam monitor phenological variations, prompting a demand for automated methods. This project develops tools to recognize Phenophase changes and predictive models for leaf phenology in deciduous broadleaf forests. Unlike single-site methods, it enhances prediction accuracy across multiple sites, focusing on the start (SOS) and end (EOS) dates of leaf growth using PhenoCam images. Steps include data labeling, preprocessing, ResNet50 CNN model development, and Generative Adversarial Networks (GANs) incorporation, aiming to anticipate key ecological events related to leaf growth.<br>  
             <a class="image-container"><img src="/assets/images/current_day_pred_after1500epoch.png" alt="Project Image"></a><br>          
        </p>
        <a href="PhenoCam-Image-Analysis-Using-CNN/Phenophase_Prediction at main · AmritaNeogi/PhenoCam-Image-Analysis-Using-CNN (github.com)" style="text-decoration: none;">Know More </a><img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"> <br><br>
    </div>
     <div id="project7" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>YOUTUBE DATA PIPELINE USING APACHE AIRFLOW</strong></h2>
        <p><i>October 2023</i></p>
        <div class="image-container"><img src="/assets/images/yt.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">            
            This YouTube Data ETL with Airflow project automates the extraction, transformation, and loading of data based on YouTube channels IDs. It uses the YouTube Data API, transforms the data, and stores it in destinations like Amazon S3. Apache Airflow schedules and orchestrates the ETL process, ensuring the data is up-to-date and reliable for analysis. 
            <a class="image-container"><img src="/assets/images/youtube.png" alt="Project Image"></a><br>
            <!-- <a class="image-container"><img src="/assets/images/uber_data_model.jpeg" alt="Project Image"></a><br> -->
            The project consists of components for data extraction, transformation, loading, Airflow integration, and error handling. Its key objectives are to automate data retrieval, ensure data cleanliness, offer flexibility in storage, provide a dependable ETL process with Airflow integration, and offer a customizable framework. In summary, it simplifies YouTube channel data ETL, benefiting data enthusiasts, analysts, and engineers.<br>
            <!-- <a class="image-container"><img src="/assets/images/NN_model_accuracy_Loss.png" alt="Project Image"></a><br>              -->
        </p>
        <a href="https://github.com/AmritaNeogi/YouTube_Data_Pipieline_Using_Airflow" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"><br><br>
    </div>
        <div id="project8" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>HOUSE PRICE PROFILER USING SNOWFLAKE DATABASE</strong></h2>
        <p><i>October 2023</i></p>
        <div class="image-container"><img src="/assets/images/houese_price.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">            
            Executed a House Price Profiler Project using Snowflake Database, resulting in the extraction of over 60,000 data entries from the Otodom website. Leveraging Bright Data, the project achieved an impressive 95% data extraction accuracy. The data was stored in Snowflake, and flattening operations reduced query response times by 40%. The dataset was enriched through the successful conversion of latitude and longitude to physical addresses for all entries, and translation of 95% of Polish texts to English using Google Translator.  
            <a class="image-container"><img src="/assets/images/overview_house.png" alt="Project Image"></a><br>
            <!-- <a class="image-container"><img src="/assets/images/uber_data_model.jpeg" alt="Project Image"></a><br> -->
            The project successfully answered 11 pivotal business questions, yielding actionable insights for stakeholders, resulting in enhanced decision-making capabilities. This project highlights skills in data extraction, transformation, and database management, showcasing a holistic approach to problem-solving in data analysis.<br>
            <!-- <a class="image-container"><img src="/assets/images/NN_model_accuracy_Loss.png" alt="Project Image"></a><br>              -->
        </p>
        <a href="https://github.com/AmritaNeogi/Data_Analytics_Project-Housing_Price_Profiler" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"><br><br>
    </div>
    <div id="project6" class="project" style="text-align: justify; font-size: 15px;">     
        <h2><strong>BREAST CANCER PREDICTION</strong></h2>
        <p><i>October 2023</i></p>
        <div class="image-container"><img src="/assets/images/breast_cancer.png" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">            
            Executed a breast cancer prediction project, crafting two models: a Logistic Regression model delivering 92.9% accuracy and a superior Neural Network model achieving 97.3% accuracy. This initiative stemmed from a dedication to enhancing early detection. By employing versatile modeling techniques and precise parameter optimization, they highlighted the transformative potential of data-driven solutions in healthcare, emphasizing the criticality of accurate early detection.
            <a class="image-container"><img src="/assets/images/overview_breastCancer.png" alt="Project Image"></a><br>
            <!-- <a class="image-container"><img src="/assets/images/uber_data_model.jpeg" alt="Project Image"></a><br> -->
            For the Logistic Regression Model, utilized historical patient data, selected relevant features, conducted thorough data preprocessing, fine-tuned model parameters for improved performance, ultimately achieving a 92.9% prediction accuracy, a significant advancement in early detection. In the case of the Neural Network Model, implemented the model using TensorFlow and Keras, experimented with multiple architectures and activation functions, closely monitored training progress, and adjusted hyperparameters to attain an impressive accuracy of 97.3%, indicating a substantial improvement in predictive capabilities.<br>
            <a class="image-container"><img src="/assets/images/NN_model_accuracy_Loss.png" alt="Project Image"></a><br>             
        </p>
        <a href="https://github.com/AmritaNeogi/Breast_Cancer_Prediction" style="text-decoration: none;">Know More </a> <img src="/assets/images/logo/github.png" alt="Python Logo" style="height: 24px; margin-right: 12px;"><br><br>
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
            Later, the data imbalance was tackled using SMOTE Technique. Each algorithm was fine-tuned for optimal performance and further achieved a 10% increase in the accuracy.<br>
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
            <a class="image-container"><img src="/assets/images/summary1.png" alt="Project Image"></a><br> 
            <a class="image-container"><img src="/assets/images/gradient descent.png" alt="Project Image"></a><br> 
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
