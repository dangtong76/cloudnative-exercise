# cloudWaveIAC
1. aws configure --profile cwave
1. dev-aws.tfvars 파일의 
   - env-prefix = "dev-<your-id>"
   - cwave-cluster-name = "<your-id>-eks"
3. cloudWave-980-LBController.tf 파일에서
   - cwave_eks_lb_controller_iam_role_name = "cwave-eks-aws-lb-controller-role-<your-id>"
4. aws eks update-kubeconfig --region ap-northeast-2 --name <cluster-name>