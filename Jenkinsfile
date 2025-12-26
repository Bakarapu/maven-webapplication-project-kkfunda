node {

    stage('git checkout')
    {
	git branch: 'development', url: 'https://github.com/Bakarapu/maven-webapplication-project-kkfunda.git'
    }
    stage('Deploy to Tomcat') {
    echo "Deploying WAR file using curl..."

    sh """
        curl -u kk:password \
        --upload-file /var/lib/jenkins/workspace/Jio-Development/target/maven-web-application.war \
        "http://15.207.14.183:8080/manager/text/deploy?path=/maven-web-application&update=true"
    """
}

}
