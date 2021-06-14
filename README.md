# Installing the F5 Container Ingress Services Operator in OpenShift

## OpenShift Operator user-guides and testing

In OpenShift, CIS can be installed manually using a a yaml deployment manifest or using the Operator in OpenShift. The CIS Operator is a packaged deployment of CIS and will use Helm Charts to create the deployment. This user-guide provide additional information and examples when using the CIS Operator in OpenShift.

Demo on YouTube [video](https://www.youtube.com/watch?v=-HLcHH_vQJE)

### Prerequisites

Create BIG-IP login credentials for use with Operator Helm charts

    oc create secret generic bigip-login  -n kube-system --from-literal=username=admin  --from-literal=password=<secret>

### Step 1

Locate the F5 Container Ingress Services Operator in OpenShift OperatorHub as shown in the diagram below. Recommend search for F5 

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-10_12-59-30.png)

### Step 2

Select the Operator to Install. In this example I am installing the latest Operator 1.7.0. Select the Install tab as shown in the diagram

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-10_13-20-27.png)

### Step 3

Install the Operator and provide the installation mode, installed namespaces and approval strategy. In this user-guide and demo I am using the defaults

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-10_13-47-45.png)

Operator will take a few minutes to install

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-10_13-50-10.png)

Once installed select the View Operator tab

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-10_13-51-02.png)

## Step 4

Now that the operator is installed you can create an instance of CIS. This will deploy CIS in OpenShift

![diagram](https://github.com/mdditt2000/operator/blob/main/diagrams/2021-06-14_14-07-36.png)



