# aws-Rekognition

In this project we build an image recognition pipeline in AWS, using two EC2 instances, S3, SQS, and Rekognition.
We create two instances lets say A and B where instance A performs object detecetion on images present in S3. When a car(with confidence >= 90%) is detected these images are sent to a specified SQS queue.
Instance B reads indexes of images from SQS as soon as these indexes become available in the queue, and performs text recognition on these images.
