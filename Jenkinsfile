pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        snap_repo = 'vprofile-snapshot'
        nexus_user = 'admin'
        nexus_pass = 'admin123'
        release_repo = 'vprofile-release'
        central_repo = 'vpro-maven-central'
        nexusip = '172.31.20.156'
        nexusport = '8081'
        nexus_grp_repo = 'vpro-maven-group'
        nexus_login = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}