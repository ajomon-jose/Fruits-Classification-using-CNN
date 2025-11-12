# Fruits-Classification-using-CNN
Business Challenge: Automatic Fruit Classification for Smart Supermarkets¶
Context
Supermarkets are increasingly investing in smart self-checkout technologies to optimize customer experience, reduce lines, and eliminate manual weighing and labeling processes for fruits and vegetables. This scenario requires an automatic image-based classification solution, integrated into checkout systems, capable of correctly identifying various types of fruits, vegetables, nuts, and seeds, even under different lighting and positioning conditions.

Business Problem
Currently, the process of weighing and identifying fruits in supermarkets is:

Manual, relying on the customer or an employee.
Prone to pricing errors.
Slow and inefficient, causing long queues at checkout.
Main Objective
Develop a computer vision solution based on deep learning (CNN) capable of automatically classifying 200 types of fruits, vegetables, nuts, and seeds with high accuracy, even in adverse conditions.

Specific Objectives
Build a robust model trained on the Fruits-360 (100x100 branch) dataset.
Integrate the model into a self-checkout prototype system.
Ensure the model performs in real-time, with inference latency below 1 second per image.
Test the model under simulated supermarket conditions (lighting, rotation, multiple angles).
Success Metrics
Metric	Target
Top-1 Accuracy	≥ 95%
Top-3 Accuracy	≥ 98%
Inference Latency	≤ 1 second
Pricing Error Reduction	≥ 30%
User Feedback (NPS)	≥ 8/10
Dataset Justification
Utilizing the Fruits-360 (100x100 branch) dataset due to:

High diversity of classes (200).
Various conditions (rotated images).
Clean, pre-segmented images (neutral background), facilitating initial generalization.
Allows for quick validation with transfer learning on real supermarket images in later stages.
Proposed Initial Technical Solution
Stage	Description
Preprocessing	Resize to 100x100, normalize pixel values
Base CNN Model	Custom CNN or pre-trained MobileNet
Optimization	Early stopping, data augmentation
Validation	Use the dataset's test set for validation
Realistic Simulation	Apply to images captured in real supermarket scenarios using smartphones
Latency Measurement	Simulate on hardware similar to checkout systems
