# Terraform

- https://www.youtube.com/watch?v=YcJ9IeukJL8&list=PLKjV8hx8vwdhLJGVUOGipsKPnMuN_GmGz&index=1

### Validate the configuration 
If the configuration is correct, it shows the configuration valid message.

``` terraform validate ```

### Format the files
It formats the file for the better readability

``` terraform fmt ```

### Output Values
- https://www.youtube.com/watch?v=rg3qZXitjEg
![image](https://user-images.githubusercontent.com/11143215/174470876-a30389b1-69c4-490e-8f1e-e90d6b234e26.png)

## Terraform resource
![image](https://user-images.githubusercontent.com/11143215/174468711-e9f9b67f-7f7d-465e-8c2c-cb534a1dc05e.png)

Here: We have Resource Type called "local_file" and this provides two bits of information
1. provider => this is the word before the underscore(_) in the resource type
2. The word following the underscore(_) represents the type fo the resource in this case it its file
      
            terraform init => Initialize the terraform 
            terraform plan => view the changes that will be done 
            terraform apply => exectute the command
      
## Without using variable
![image](https://user-images.githubusercontent.com/11143215/174469708-585312cf-f88d-4d6c-b568-0cc6afe14b83.png)

## After using variables
![image](https://user-images.githubusercontent.com/11143215/174469724-3c307b52-0361-4f3b-9ca2-c8ef7b1db09b.png)

## Variable types
### List
![image](https://user-images.githubusercontent.com/11143215/174470244-3e55d312-2e5b-40a9-aaa4-eed5f29f36f1.png)
### Map
![image](https://user-images.githubusercontent.com/11143215/174470285-f9d45bbb-8e39-4608-9915-678e4e459e47.png)

### List of a type
![image](https://user-images.githubusercontent.com/11143215/174470315-ab2dd709-f15d-4031-b4d2-1c43ceda9fce.png)

### Map of a type
![image](https://user-images.githubusercontent.com/11143215/174470343-90d0ab41-6156-42e9-8ab0-35a36c265d3a.png)

## Objects
![image](https://user-images.githubusercontent.com/11143215/174470410-aeb9a938-35dc-4003-bceb-d9ccf93ecc8c.png)

## Tuples
![image](https://user-images.githubusercontent.com/11143215/174470463-d082cfc7-0fe7-438b-99b5-9d701430afea.png)

# Life Cycle Rules
If we want to update the resources and then apply the changes, by default the old resource will be deleted first and then only the new
resources are created. This might not be good case
![image](https://user-images.githubusercontent.com/11143215/174471091-b2d61a1d-87d3-47c2-81c7-64169926d27d.png)

### create_before_destroy
By using this the resources will be created first and then only the old resources will be deleted.
![image](https://user-images.githubusercontent.com/11143215/174471161-d6d738d8-2afa-4337-93a9-15c0ed3ffa20.png)

### prevent_destroy (when used terraform will prevent the destruction of the resource)
![image](https://user-images.githubusercontent.com/11143215/174471215-8ca20616-97c8-4005-95c6-7be23a926790.png)



