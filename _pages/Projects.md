---
layout: single
title: 
permalink: /Projects/
date: 2023-8-13
categories: pages
toc: false
toc_label: "Project"
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
        box-sizing: border-box;
        padding: 20px;
        border: 1px solid #ccc;
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
        float: left;
        width: 20%; /* Adjust the width as needed */
        padding-right: 20px; /* Add space between legend and projects */
    }

    .legend ul {
        list-style: none;
        padding: 0;
    }

    .legend li {
        margin: 10px 0;
        font-size: 14px; /* Adjust the font size for the legend */
    }

    /* Style for the title */
    h1 {
        color: blue; /* Change the title text color to blue */
    }
</style>

<!-- Title of the page in blue -->
<h1>Projects</h1>

<!-- Legend on the left -->
<div class="legend">
    <ul>
        <li><a href="#project1">Identifying Leaf Phenology</a></li>
        <li><a href="#project2">Credit Card Fraud Detection</a></li>
        <li><a href="#project3">Salary Prediction</a></li>
        <li><a href="#project4">Image Classifier Using CNN</a></li>
    </ul>
</div>

<div class="project-container">
    <div id="project1" class="project" style="text-align: justify; font-size: 17px;">     
        <h2><strong>Identifying Leaf Phenology of Deciduous Broadleaf Forests from PhenoCam Images</strong></h2>
        <p><i>In Progress</i></p>
        <div class="image-container"><img src="/assets/images/decidousForest.jpg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
            <!-- Project description -->
        </p>
        <a href="https://github.com/AmritaNeogi/PhenoCam-Image-Analysis-Using-CNN">[GitHub Link]</a>
    </div>
    
    <div id="project2" class="project" style="text-align: justify; font-size: 17px;">     
        <h2><strong>Credit Card Fraud Detection</strong></h2>
        <p><i>Aug 2023</i></p>
        <div class="image-container"><img src="/assets/images/credit_card.jpeg" alt="Project Image"></div>
        <p style="line-height: 1.5; font-size: 15px;">
            <!-- Project description -->
        </p>
        <a href="https://github.com/AmritaNeogi/Data-Science-Project-Credit-Card-Fraud-Detection">[GitHub Link]</a>
    </div>

    <!-- Add more project divs similarly -->
</div>
