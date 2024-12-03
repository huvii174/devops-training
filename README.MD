# Project Training

## Task 1: Prepare the Application for Deployment
- **Objective:** Understand the application and prepare it for deployment in a containerized environment.
  1. **Read the source code** to familiarize yourself with the application's functionality and structure.
  2. **Write a Dockerfile** to containerize the application.
      - Optimize the Dockerfile for smaller image size and faster build times.
  3. **Create an Elastic Container Registry (ECR) on AWS** to store the Docker images.
  4. **Automate the build and push process:**
      - Use **AWS CodeBuild** and **AWS CodePipeline** to configure an automated pipeline.
      - Integrate **GitHub** with CodePipeline to trigger builds on new commits.

## Task 2: Create an Amazon EKS Cluster
- **Objective:** Set up a Kubernetes environment on AWS.
  1. Use **eksctl** or **AWS CLI** to create an EKS cluster with **2 nodes**.
  2. Configure the local machine to connect to the EKS cluster:
      - Install necessary tools such as `kubectl` and configure credentials.
      - Verify the connection by listing the nodes in the cluster.

## Task 3: Deploy PostgreSQL to EKS
- **Objective:** Set up a database in the Kubernetes cluster.
  1. Deploy a **PostgreSQL instance** on EKS using Persistent Volume Claims (PVC) for data storage.
  2. Enable **port forwarding** from EKS to the local machine.
  3. Connect to the PostgreSQL database using a database client (e.g., pgAdmin, DBeaver).
  4. Execute the SQL queries provided in the `db` folder to set up the database schema and seed data.

## Task 4: Run the Application Locally with Docker
- **Objective:** Test the application locally in a containerized environment.
  1. Use the Dockerfile to build and run the application locally.
  2. Connect the application to the deployed PostgreSQL database.
  3. Test API calls to verify that the application interacts correctly with the database.

## Task 5: Deploy the Application to EKS
- **Objective:** Deploy the complete application stack in the Kubernetes cluster.
  1. Create a Kubernetes manifest to deploy the application to EKS.
  2. Store the database password securely in Kubernetes Secrets.
  3. Update the application deployment to reference the secret for database credentials.
  4. Test the deployed application to ensure it works as expected.
