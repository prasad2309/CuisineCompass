# CuisineCompass: A Cloud-Based Restaurant Recommendation System

This project implements a Dining Concierge Chatbot using AWS services. The chatbot can take user inputs such as location, cuisine preference, dining time, number of people, and email, and then push this information to an SQS queue.

## Table of Contents
- [Architecture](#architecture)
- [Features](#features)
- [Setup](#setup)
- [Frontend Deployment](#frontend-deployment)
- [API Implementation](#api-implementation)
- [Chatbot Implementation](#chatbot-implementation)
- [Integration](#integration)
- [Testing](#testing)

## Architecture

1. **Frontend:** Hosted in an AWS S3 bucket, serving a static website for interacting with the chatbot.
2. **API Gateway:** Exposes the API to the frontend.
3. **AWS Lambda (LF0):** Handles API requests, forwards user messages to the Lex chatbot.
4. **Amazon Lex:** Manages the chatbot logic.
5. **AWS Lambda (LF1):** Code hooks for Lex intents, processing user inputs, and sending data to SQS.
6. **Amazon SQS:** Queue to hold dining suggestions requests.

## Features

- **Frontend:** Simple UI to interact with the chatbot.
- **API:** RESTful API to handle user messages.
- **Chatbot:** Lex-based chatbot with intents for greeting, thanking, and dining suggestions.
- **Integration:** Full integration of Lex chatbot with the API and frontend.
