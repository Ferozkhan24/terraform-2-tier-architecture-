## RDS `main`

```
resource "aws_db_instance" "db" {
  allocated_storage   = 20
  db_name             = "mydb"
  engine              = "mysql"
  engine_version      = "8.0"
  instance_class      = "db.t3.micro"
  username            = var.db_username
  password            = var.db_password
  skip_final_snapshot = true
  publicly_accessible = true

  tags = {
    Name = var.name
  }
}
output "endpoint" {
  value = aws_db_instance.db.endpoint
}
```
