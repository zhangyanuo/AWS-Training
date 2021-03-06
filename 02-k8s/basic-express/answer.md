- 1.在本地安装 kubectl 命令行以及任意 k8s 运行环境（MiniKube / Docker Desktop / 其他）
- 2.简述 kubectl logs / describe / apply / delete 命令的功能
    - Logs:可以查看正在运行的pod的log信息
    - Describe:做debug的时候比较有用，查看之前时间的状态原因
    - Apply:对部署在k8s的资源进行修改或者新增
    - Delete:服务有性能问题时，重启时delete pod 删掉不属于集群中的资源
- 3.将示例中的 Node.js 应用（或自定义其他工程）通过 Deployment 部署，经过Service组织后由Ingress暴露出可被访问的API（使用kubectl apply）
- 4.使用 kubectl get查看本地运行的所有pod，deployment，service，使用kubectl describe查看pod，deployment的详细信息
- 5.使用 kubectl logs 查看正在运行的pod的日志
- 6.使用 kubectl port-forward 命令将本地请求直接转发到 pod