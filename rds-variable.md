rds-variable

```
variable "db_username" {
  description = "Database admin username"
  type        = string
}

variable "db_password" {
  description = "Database admin password"
  type        = string
  sensitive   = true
}

variable "name" {
  description = "Name tag for RDS instance"
  type        = string
}
```