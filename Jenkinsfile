pipeline {

	agent any

	tools {
        maven "Maven"
        jdk "JDK"
    }

    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'bako2442000'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = 'localhost'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'pro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }
	
    stages{

        stage('BUILD'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }

    }
}
