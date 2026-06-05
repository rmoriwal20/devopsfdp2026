You have one new message.

Skip to content
Using GLA University Mail with screen readers

1 of 3,218
CODE
Inbox

Medha Kirti
Attachments
Thu, Jun 4, 1:09 PM (22 hours ago)
PFA Regards, Dr. Medha Kirti GLA University

Medha Kirti <medha.kirti@gla.ac.in>
Attachments
11:10 AM (0 minutes ago)
to me

 3 Attachments
  •  Scanned by Gmail
pipeline {
    agent any

    environment {
        IMAGE_NAME = "myapp"
        CONTAINER_NAME = "myapp-container"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/USERNAME/REPOSITORY.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ${IMAGE_NAME}:latest .'
            }
        }

        stage('Stop Existing Container') {
            steps {
                sh '''
                docker stop ${CONTAINER_NAME} || true
                docker rm ${CONTAINER_NAME} || true
                '''
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker run -d \
                --name ${CONTAINER_NAME} \
                -p 80:80 \
                ${IMAGE_NAME}:latest
                '''
            }
        }
    }
}
Jenkinsfile.txt
Displaying Jenkinsfile.txt.
