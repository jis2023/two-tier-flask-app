
pipeline{
    
    agent any;
    
    stages{
        stage("Code Clone"){
            steps{
                git url: "https://github.com/jis2023/two-tier-flask-app.git" , branch: "master"
            }
        }

        stage("Build"){
            steps{
                sh "docker build -t two-tier-flask-app ."
            }
            
        }
        stage("Test"){
            steps{
                echo "Developer / Tester tests likh ke dega..."
            }
            
        }
        stage("Deploy"){
            steps{
                sh "docker compose up -d --build flask-app"
            }
        }
    }
}
