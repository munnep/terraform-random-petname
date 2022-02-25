# Module to use

Generates a private name for you pet

# How to

## Repository
The repository name of your module to use in a private registry should have the format of
```
terraform-<PROVIDER>-<NAME>
```
In this case it is made as terraform-random-petname


## Tags
You should make a tag with a version number
- Go to your repository and click tags  
![](media/2022-02-25-14-04-00.png)  
- Click on releases 
- draft a new release  
![](media/2022-02-25-14-04-51.png)  
- Choose a tag 
- tag name should be format ```x.y.z```  
![](media/2022-02-25-14-05-35.png)  
- select Publish release  
![](media/2022-02-25-14-06-07.png)  

## Import it in the private registry
- Log into your terraform Cloud
- Click on registry
- Click on Publish Module  
![](media/2022-02-25-14-07-42.png)    
- Select the location where your repository exists  
![](media/2022-02-25-14-08-17.png)    
- select your module  
![](media/2022-02-25-14-08-40.png)  
- select publish module  
![](media/2022-02-25-14-08-56.png)  
- It should now be available to be used  
```
module "petname" {
  source  = "app.terraform.io/patrickmunne/petname/random"
  version = "0.0.2"
}
```

## Use the private module

Create a repository that has the following files

https://github.com/munnep/tfc_use_private_module

You can run the code from Terraform Cloud
![](media/2022-02-25-14-42-48.png)  