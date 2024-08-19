pipeline {
    agent any
    environment {
        AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
        AWS_DEFAULT_REGION = "ap-south-1"
    }

    stages {
        stage('git cloning') {
            steps {
                echo 'cloning git repo'
                git url:"https://github.com/MiksVeg/Flask-Monitoring-App.git", branch: "main"
            }
        }
        stage('build') {
            steps {
                echo 'building the image'
                sh "docker build -t monitoring-flask-app ."
                
            }
        }
        stage('dockerhub') {
            steps {
                echo 'pushing to dockerhub'
                withCredentials([usernamePassword(credentialsId:"dockerhub-cred",usernameVariable:"user",passwordVariable:"pass")]){
                sh "docker login -u ${env.user} -p ${env.Pass}"
                sh "docker tag monitoring-flask-app ${env.user}/monitoring-flask-app:latest"
                sh "docker push  ${env.user}/monitoring-flask-app:latest"
                }
            }
        }
        stage('k8s') {
            steps {
                echo 'Hello World'
                sh "aws eks update-kubeconfig --name kube-cluster"
                sh "kubectl apply -f deployment.yaml"
                sh "kubectl apply -f service.yaml"
            }
        }
    }
}
