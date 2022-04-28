pipeline {
agent any
stages{
        stage(gitcheckout){
            steps{
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/kliakos/sparkjava-war-example.git']]])
}

}
stage(mavenstage){
            steps{
              echo "this is maven stage"
}

}
stage(deploystage){
            steps{
              echo "this is deploy stage"
}

}


    





}


}
