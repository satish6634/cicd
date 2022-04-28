pipeline {
agent any
tools{
jdk 'myjava'
maven 'mymvn'

}
stages{
        stage(gitcheckout){
            steps{
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/kliakos/sparkjava-war-example.git']]])
}

}
stage(mavenstage){
            steps{
              sh 'mvn package'
}

}
stage(deploystage){
            steps{
              sh '/var/lib/jenkins/workspace/testpipeline/target/sparkjava-hello-world-1.0.war /opt/apache-tomcat-9.0.62/webapps'
}

}


    





}


}
