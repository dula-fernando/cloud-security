# IAM Enumeration Cheat Sheet

## List IAM Users
    aws iam list-users

## List User Permissions
### List Attached Managed Policies
    aws iam list-attached-user-policies --user-name [user-name]

### List Inline Policies
    aws iam list-user-policies --user-name [user-name]

### Display Inline Policy Details
    aws iam get-user-policy --user-name [user-name] --policy-name [policy-name]

## List IAM Groups and Permissions
### List Groups for a User
    aws iam list-groups-for-user --user-name [user-name]

### List Group Policies
    aws iam list-attached-group-policies --group-name [group-name]

    aws iam list-group-policies --group-name [group-name]

### List Inline Group Policy Details
    aws iam get-group-policy --group-name [group-name] --policy-name [policy-name]

## List IAM Roles and Permissions
### List All Roles
    aws iam list-roles

### Get Role Details
    aws iam get-role --role-name [role-name]

### List Attached Policies to Role
    aws iam list-attached-role-policies --role-name [role-name]

### List Inline Policies
    aws iam list-role-policies --role-name [role-name]

### Get Inline Role Policy Details
    aws iam get-role-policy --role-name [role-name] --policy-name [policy-name]

## Get and Decode Policy Documents
    aws iam get-policy --policy-arn [policy-arn]

    aws iam get-policy-version --policy-arn [policy-arn] --version-id [version-id]

## View Full IAM Snapshot (Dump All IAM Permissions)
    aws iam get-account-authorization-details

> Use this to build a full IAM permissions map. Add --filter to target roles/users/groups specifically.

