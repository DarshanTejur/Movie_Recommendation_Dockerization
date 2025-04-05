# 🎬 Movie Recommendation System

## 📖 Overview  
  This is a **DevOps-integrated Django-based Movie Recommendation System**. The project is containerized using Docker and features a GitHub Actions workflow for continuous integration and automated testing.

## ✨ Features  
   **Django Backend**: A functional recommendation system built with Django.
   **CI/CD**: Automated testing pipeline powered by GitHub Actions.
   **Dockerized**: Complete containerization for easy setup and portability.

## 🛠️ Technologies  
  ### Backend  
  - Django (Python)  
  - Pandas, NumPy, SciPy  
  - REST API  

  ### DevOps  
  - Docker  
  - GitHub Actions (CI/CD)

## 📁 Folder Structure  

```
Movie_Recommendation_Dockerization/
├── src/                    # Django project and app code
├── requirements.txt        # Python dependencies
├── Dockerfile              # Docker image instructions
├── .github/workflows/
│   └── cicd.yml            # CI/CD pipeline file
```

## 🚀 Step-by-Step Setup Instructions  
   You don’t need to manually configure internals — just follow the steps:

### 1. Clone the Repo  
    ```
    git clone https://github.com/DarshanTejur/Movie_Recommendation_Dockerization.git  
    cd Movie_Recommendation_Dockerization  
    ```

### 2. Prerequisites  
  Ensure you have:
    - Docker
    - Git
    
### 3. Build and Run the Docker Container  
    ```
    docker build -t movie-recommendation .  
    docker run -p 8000:8000 movie-recommendation  
    ```
  Open in browser: [http://localhost:8000](http://localhost:8000)

### 4. View Running Containers  
    ```
    docker ps  
    ```

  To stop and remove:
    
        docker stop <container_id>  
        docker rm <container_id>  

## 🔁 CI/CD Pipeline (GitHub Actions)  
  This project uses a GitHub Actions workflow that runs on every push or pull request to the `main` branch. It includes:

  - Checking out the code  
  - Setting up Python 3.8  
  - Installing dependencies  
  - Running Django tests  

### CICD File Location:  
`.github/workflows/cicd.yml`

## 🧪 How I Set This Up (Step-by-Step Guide)

### Docker Setup  
- Wrote a `Dockerfile` to create an isolated image of the Django project.  
- Exposed port 8000 and used `python src/manage.py runserver` to launch the app inside the container.

### GitHub Actions - CI/CD Workflow  
  Steps I followed:
```
mkdir -p .github/workflows  
touch .github/workflows/cicd.yml  
```

  Defined actions:
    - Install Python 3.8  
    - Install dependencies  
    - Run tests automatically on push/pull request  

  Git operations:
```
git add .  
git commit -m "Add CI/CD pipeline using GitHub Actions"  
git push origin main  
```

### Checked GitHub Actions  
  1. Go to your GitHub repo  
  2. Click on the **Actions** tab  
  3. You’ll see the workflow automatically running!

Let me know if you'd like badges (e.g., build passing), screenshots, or contributor credits added!
