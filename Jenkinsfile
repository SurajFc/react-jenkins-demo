pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rvf /var/www/react_jenkins"
                sh "sudo cp -rvf ${WORKSPACE}/build/ /var/www/react_jenkins/"
            }
        }
    }
}