# Migrating the Database to RDS

This README documents the changes made to the YAML template for migrating the MySQL database from a local instance on the EC2 instance to a managed RDS database.

![m4ch-lab-start-arch](https://github.com/andres-pulecio/aws-cloudformation-templates/assets/53886913/e56c96e5-49ae-42f6-8cb4-a8e0d315ee3b)

## Changes Made

1. An `AWS::RDS::DBInstance` resource was added to create an RDS MySQL instance instead of the local database.
2. The properties of the `DBInstance` were configured, including the identifier, instance type, engine, users, passwords, etc.
3. The `DBSubnetGroup` resource was removed as the RDS instance handles subnet allocation.
4. The `DBSecurityGroup` was removed; instead, the default VPC security group is used.
5. The `DBHost` property in the `CafeInstance` EC2 instance was updated to point to the RDS endpoint.
6. Scripts in the `UserData` of `CafeInstance` that created the local database and populated it with sample data were removed.
7. The remaining shell scripts in `UserData` were modified to connect to the RDS instance instead of the local database.
8. Tests were conducted to validate that the `CafeInstance` application can connect and operate correctly with the RDS database.
