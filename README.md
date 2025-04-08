# Audible Insights: Intelligent Book Recommendations

**Audible Insights** is an intelligent book recommendation system designed to provide personalized audiobook suggestions based on user preferences and listening patterns. By analyzing detailed Audible book data, including ratings, reviews, genres, and listening times, this project aims to create a more tailored audiobook discovery experience.

## Features

- **Personalized Recommendations:** Recommends audiobooks based on user preferences and listening behaviors.
- **Data-Driven Insights:** Analyzes reviews, ratings, and other attributes to suggest high-quality audiobooks.
- **Genre Filtering:** Offers recommendations based on preferred genres and book categories.
- **Advanced Clustering:** Uses machine learning clustering to group similar audiobooks, improving recommendation accuracy.

## Technologies Used

- **Python:** For data analysis and recommendation logic.
- **Pandas & NumPy:** For data manipulation and handling large datasets.
- **Scikit-learn:** For clustering algorithms and machine learning models.
- **Matplotlib/Seaborn:** For data visualization and insights.
- **Jupyter Notebook:** For project development and experimentation.

## Getting Started

### Prerequisites

Before running this project, ensure you have the following installed:

- Python 3.x
- Required Python libraries (can be installed via `requirements.txt`)

### Installation

1. Clone the repository:
   ``` bash
   git clone https://github.com/your-username/audible-insights.git
   cd audible-insights

2. Install the required libraries:
   ```  bash
   pip install -r requirements.txt


### Running the Project

1. Load the dataset into the environment.
   
2. Execute the recommendation system Jupyter notebook cell by cell.
   - Open the Jupyter Notebook in your browser (e.g., `http://your-ec2-ip:8888`).
   - Navigate to the notebook file and run each cell sequentially to load data, process it, and generate recommendations.

### AWS Hosting Details

To host this project on AWS, you can follow the steps below:

1. Set up an AWS account if you don’t have one already at [AWS Sign Up](https://aws.amazon.com).

2. Launch an EC2 instance:
   - Choose an appropriate instance type (e.g., `t2.micro` for small-scale testing).
   - Use an Ubuntu AMI to install Python, Jupyter Notebook, and the required libraries.
   - Set up security groups to allow SSH (port 22) for access and HTTP (port 80) if you want a web interface.

### Install required dependencies on your EC2 instance:

1. Connect to your EC2 instance via SSH:
   ``` bash
   ssh -i your-key.pem ubuntu@your-ec2-ip


1. Install Python, pip, and other dependencies as mentioned in the "Installation" section.

2. Upload your dataset to the EC2 instance or use an S3 bucket to store it.

3. Launch Jupyter Notebook:

   - Install Jupyter Notebook:
     ``` bash
     pip install notebook
     ```

   - Start the Jupyter server:
     ``` bash
     jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser
     ```


4. Access the notebook from a web browser by navigating to `http://your-ec2-ip:8888`.

### Contributing
Feel free to fork the project, open issues, and submit pull requests. All contributions are welcome



### Deploying on AWS EC2
### 1. Launch an EC2 instance:

- Go to the [AWS Management Console](https://console.aws.amazon.com/).
- Navigate to **EC2** and click on **Launch Instance**.
- Select an appropriate instance type (e.g., `t2.micro` for testing).
- Configure your instance settings, including selecting a **key pair** that you can use for SSH access.
- Ensure that the **Security Group** for your instance allows inbound traffic on:
  - **Port 8501** for Streamlit (default port)
  - **Port 22** for SSH (to access the instance remotely)
  
### 2. SSH into your EC2 instance:

After launching the instance, you can SSH into your EC2 instance using the following command:

``` bash
ssh -i your-key.pem ubuntu@your-ec2
