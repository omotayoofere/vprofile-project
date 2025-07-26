pipeline {
    agent any
    tools {
        jdk "JDK17"
        maven "MAVEN3.9"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_PASS = 'admin'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.80.15'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
        NEXUS_USER = 'admin'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}