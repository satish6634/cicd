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
              echo "this is deploy stage"
}

}


    





}


}
