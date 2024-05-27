Terraform IAC (BASIC): Terraform is coding language HashiCorp Configuration Language (HCL), or optionally JSON.
                       Using this we can create a resources on cloud platforms like AWS/AZURE/GCP.
                       Infrastructure as code . We can create servers using by writing code in terraform.
                       
Terraform Commands :   There are serverl commands are available in Terraform using those command we can create a resource in colud.
                       Main commands are follow.

Commands: 

terraform version -                        Displays the version of Terraform and all installed plugins  .


                            //Format Your Terraform Code  // 

                           
terraform fmt                            — Format your Terraform configuration files using the HCL language standard.

terraform fmt --recursive                — Also format files in subdirectories

terraform fmt --diff                     — Display differences between original configuration files and formatting changes.


                             //Initialize Your Directory//

 terraform init                         — In order to prepare the working directory for use with Terraform, the terraform init command performs Backend Initialization, 
                                          Child Module Installation, and Plugin Installation.

terraform init -get-plugins=false       — Initialize the working directory, do not download plugins.

terraform init -lock=false              — Initialize the working directory, don’t hold a state lock during backend migration.

terraform init -input=false             — Initialize the working directory, and disable interactive prompts.

terraform init -migrate-state           — Reconfigure a backend, and attempt to migrate any existing state.

terraform init -verify-plugins=false    — Initialize the working directory, do not verify plugins for Hashicorp signature         



                               //Download and Install Modules//

terraform get                           — Download and installs modules needed for the configuration.

terraform get -update                   — Check the versions of the already installed modules against the available modules and installs the newer versions if available.


                                 //Validate Your Terraform Code//

terraform validate                      — Validate the configuration files in your directory and does not access any remote state or services.
                                          terraform init should be run before this command.

terraform validate -json               — To see easier the number of errors and warnings that you have.       

                                //Plan Your Infrastructure//
                                
terraform plan                         — Plan will generate an execution plan, showing you what actions will be taken without actually performing the planned actions.

terraform plan -out=<path>             — Save the plan file to a given path. Can then be passed to the terraform apply command.

terraform plan -destroy                — Create a plan to destroy all objects rather than the usual actions     


                                 //Deploy Your Infrastructure//

terraform apply                        — Create or update infrastructure depending on the configuration files. By default, 
                                         a plan will be generated first and will need to be approved before it is applied.

terraform apply -auto-approve          — Apply changes without having to interactively type ‘yes’ to the plan. Useful in automation CI/CD pipelines.

terraform apply <planfilename>        — Provide the file generated using the terraform plan -out command. If provided, 
                                        Terraform will take the actions in the plan without any confirmation prompts.

terraform apply -lock=false           — Do not hold a state lock during the Terraform apply operation. 
                                        Use with caution if other engineers might run concurrent commands against the same workspace.

terraform apply -parallelism=<n>       — Specify the number of operations run in parallel.

terraform apply -var="environment=dev" — Pass in a variable value.

terraform apply -var-file="varfile.tfvars" — Pass in variables contained in a file.

terraform apply -target=”module.appgw.0" — Apply changes only to the targeted resource.

                                 //Destroy Your Infrastructure//   


 
terraform destroy                           — Destroy the infrastructure managed by Terraform.

terraform destroy -target=”module.appgw.0"  — Destroy only the targeted resource.

terraform destroy --auto-approve            — Destroy the infrastructure without having to interactively type ‘yes’ to the plan. Useful in automation CI/CD pipelines.  


                                 // ‘Taint’ or ‘Untaint’ Your Resources //

              Use the "taint" command to mark a resource as not fully functional. It will be deleted and re-created.

terraform taint vm1.name                   — Taint a specified resource instance.

terraform untaint vm1.name                 — Untaint the already tainted resource instance.   


                                 // Refresh the State File//

 terraform refresh               — Modify the state file with updated metadata containing information on 
                                   the resources being managed in Terraform. Will not modify your infrastructure                                


                               // View Your State File //
                               
terraform show                      — Show the state file in a human-readable format.

terraform show <path to statefile>  — If you want to read a specific state file, you can provide the path to it. If no path is provided, the current state file is shown.

                             // 

                                                           

                
