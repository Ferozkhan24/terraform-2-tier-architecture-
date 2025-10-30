## Root `main.tf`

```
module "ec2" {
  source   = "./modules/ec2"
  key_name = "Feroz"
  name     = "Feroz-EC2-Server" 
}

module "rds" {
  source       = "./modules/rds"
  db_username  = "admin"
  db_password  = "feroz123"
  name         = "Feroz-RDS-Database"   
}

output "ec2_public_ip" {
  value = module.ec2.public_ip
}

output "rds_endpoint" {
  value = module.rds.endpoint
}
```
