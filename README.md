# MNIST-Digit-Classifier
# Overview

A web application that recognizes handwritten digits (0-9) using a machine learning model trained on the MNIST dataset. Users can either draw digits on a canvas or upload images for classification.
# Features

    Interactive Drawing Canvas: Draw digits with mouse or touch input

    Image Upload: Classify digits from uploaded images

    Real-time Preview: Shows how the model sees your input (28x28 pixels)

    FastAPI Backend: Robust API for digit classification

    Mobile-Friendly: Works on both desktop and mobile devices

# Components

    Machine Learning Model (train_model.py):

        Random Forest classifier trained on MNIST dataset

        Achieves ~97% accuracy

        Serialized using pickle for easy deployment

    Backend API (main.py):

        FastAPI server with CORS support

        Image preprocessing pipeline:

            Grayscale conversion

            Resizing to 28x28

            Color inversion (MNIST format)

            Normalization

        Two endpoints:

            /predict_image: Classifies uploaded images

            /test_model: Health check endpoint

    Frontend (index.html):

        Interactive drawing canvas

        Image upload functionality

        Real-time classification results

        Responsive design for all devices

# Technical Details

    Model: Random Forest with 100 estimators

    Input: 28x28 grayscale images (white digit on black background)

    Output: Predicted digit (0-9)

    Preprocessing: Automatic conversion of user input to MNIST format

# API Endpoints

    POST /predict_image: Accepts image file, returns JSON with prediction

    GET /test_model: Health check endpoint

# Customization

    To retrain the model, modify train_model.py and run it

    Adjust the frontend styling in index.html

    Change the model parameters in main.py
