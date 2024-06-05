pipeline {
    agent any
    environment {
        DOCKERHUB_USERNAME = 'abdullahdaniyal1234'
        DOCKERHUB_PASSWORD = 'superflies2026'
        DOCKERHUB_REPO = 'abdullahdaniyal1234'
    }
    stages {
        stage('i211234-Checkout') {
            steps {
                script {
                    echo 'Checking out code...'
                    checkout scm
                }
            }
        }
        stage('i211234-Build and Push Auth Image') {
            steps {
                script {
                    echo 'Building and pushing Auth Docker image...'
                    dir('Auth') {
                        sh 'docker build -t ${DOCKERHUB_REPO}/auth-service:latest .'
                        sh 'echo $DOCKERHUB_PASSWORD | docker login -u $DOCKERHUB_USERNAME --password-stdin'
                        sh 'docker push ${DOCKERHUB_REPO}/auth-service:latest'
                    }
                }
            }
        }
        stage('i211234-Build and Push Classrooms Image') {
            steps {
                script {
                    echo 'Building and pushing Classrooms Docker image...'
                    dir('Classrooms') {
                        sh 'docker build -t ${DOCKERHUB_REPO}/classrooms-service:latest .'
                        sh 'echo $DOCKERHUB_PASSWORD | docker login -u $DOCKERHUB_USERNAME --password-stdin'
                        sh 'docker push ${DOCKERHUB_REPO}/classrooms-service:latest'
                    }
                }
            }
        }
        stage('i211234-Build and Push Event-Bus Image') {
            steps {
                script {
                    echo 'Building and pushing Event-Bus Docker image...'
                    dir('event-bus') {
                        sh 'docker build -t ${DOCKERHUB_REPO}/eventbus-service:latest .'
                        sh 'echo $DOCKERHUB_PASSWORD | docker login -u $DOCKERHUB_USERNAME --password-stdin'
                        sh 'docker push ${DOCKERHUB_REPO}/eventbus-service:latest'
                    }
                }
            }
        }
        stage('i211234-Build and Push Post Image') {
            steps {
                script {
                    echo 'Building and pushing Post Docker image...'
                    dir('Post') {
                        sh 'docker build -t ${DOCKERHUB_REPO}/post-service:latest .'
                        sh 'echo $DOCKERHUB_PASSWORD | docker login -u $DOCKERHUB_USERNAME --password-stdin'
                        sh 'docker push ${DOCKERHUB_REPO}/post-service:latest'
                    }
                }
            }
        }
        stage('i211234-Build and Push Frontend Image') {
            steps {
                script {
                    echo 'Building and pushing Frontend Docker image...'
                    dir('client') {
                        sh 'docker build -t ${DOCKERHUB_REPO}/frontend-service:latest .'
                        sh 'echo $DOCKERHUB_PASSWORD | docker login -u $DOCKERHUB_USERNAME --password-stdin'
                        sh 'docker push ${DOCKERHUB_REPO}/frontend-service:latest'
                    }
                }
            }
        }
    }
}
