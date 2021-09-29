pipeline {
    agent any
    stages {
        ///
        stage('clone') {
            steps {
		        git 'https://github.com/jleetutorial/maven-project.git'
            }
        }
        ///
        stage('build') {
            steps {
        	
        		sh "mvn package"
        	
        	
            }
        }
        ///
        stage('Archive the artifact') {
            steps {
        		archiveArtifacts artifacts: "**/*.war", followSymlinks: false
            }
        }
        /// deploy step
        stage('Deploy') {
            steps {
        		deploy adapters: [
        		    tomcat9(credentialsId: '8689a8e6-32d3-412b-9a7c-90e2c2af05ba',
        		    path: '', url: 'http://172.31.12.86:8888/')
        		    ], 
        		contextPath: null, war: '**/*.war'
            }
        }
    }
}
