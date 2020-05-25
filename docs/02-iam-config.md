# Creating an IAM user through CLI

To create an IAM user using the AWS CLI:
```
aws iam create-user --user-name Jacob
```
Output:
```
User:
  Arn: *****
  CreateDate: '2020-05-24T22:25:58+00:00'
  Path: /
  UserId: *****
  UserName: Jacob
```
# Configuring Billing Alerts through CLI

Configuring billing alerts is very important to make sure that you don't accidentally rack up a huge bill that you can't pay. I've read too many stories of people leaving on large instances for days on end and being charged thousands of dollars! To configure billing alerts on the AWS CLI:
```
 aws budgets create-budget --account-id ***** --budget file://budget.json --notifications-with-subscribers file://notifications-with-subscribers.json
 ```
 The files for [budget.json](budgets.json) and [notifications-for-subscribers](notifications-for-subscribers) that I used are linked.
 Verifying that the budget alert was created by checking the AWS console: ![](images/aws-billing-alert.png)

# Creating Access Keys through CLI
To create access keys through the CLI:
```
aws iam create-access-key
```
Output:
```
AccessKey:
  AccessKeyId: *****
  CreateDate: '2020-05-24T23:02:35+00:00'
  SecretAccessKey: *****
  Status: Active
```


Alternatively, you can import the [AWS Powershell Module](https://aws.amazon.com/powershell/) to do so. In this case, you can use the command:
```
New-IAMAccessKey
```

# Creating a Group
Per the AWS best practices, I am going to create a group and attach the desired permissions to the group, and then assign the user to the group.
Creating an 'Admins' group:
```
aws iam create-group --group-name Admins
```
Output:
```
Group:
  Arn: *****
  CreateDate: '2020-05-24T23:07:46+00:00'
  GroupId: *****
  GroupName: Admins
  Path: /
```
# Adding user to group
Adding the Jacob IAM user to the new Admins group:
```
aws iam add-user-to-group --user-name Jacob --group-name Admins
```
# Attaching policy to group
Attaching the 'AdministratorAccess' policy to the new Admins group:
```
aws iam attach-group-policy --policy-arn arn:aws:iam::aws:policy/AdministratorAccess --group-name Admins
```
