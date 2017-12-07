---

copyright:

  years: 2015, 2017

lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 管理用户和访问策略
{: #iamusermanage}

根据您有权管理的访问权选项，可以查看和管理整个帐户或组织中的用户。作为帐户所有者，您可以通过当前帐户中由您管理并向用户分配了访问权的任何访问权选项来管理用户。
{:shortdesc}

## 管理用户

要管理帐户中的用户，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **帐户** &gt; **用户**。“用户”窗口将显示用户列表，其中包含当前所选帐户的电子邮件地址。
2. 选择用户名，或者单击**操作**菜单中的**管理用户**。
3. 然后，根据需要执行的操作，可以选择除去用户，分配新策略或管理用户的现有访问权。

有关管理每种类型访问权的其他信息，请查看以下各部分。

如果需要查看您已添加到的帐户中为您分配的访问权，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权** &gt; **用户**。
2. 选择您的姓名。
3. 查看为您分配的角色。

如果需要其他特权，您必须联系组织管理员或帐户所有者来更新 Cloud Foundry 角色，或者联系服务或服务实例的管理员来更新服务策略。

有关用于管理帐户、组织和空间的 CLI 命令的详细信息，请参阅[用于管理帐户、组织和角色的命令](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_acctorg)。

## Cloud Foundry 访问权
{: #iammancfser}

要管理对帐户组织和空间的访问权，您必须是帐户所有者、组织管理员或空间管理员：

1. 在菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权** &gt; **用户**。
2. 选择要编辑其角色的用户名。
3. 在 Cloud Foundry 部分的**操作**菜单中，可以执行以下操作：

  * 从组织中除去用户
  * 编辑组织角色
  * 编辑空间角色

如果您是某个组织的管理员，而某个用户还不是该组织的成员，那么可以通过单击**分配组织**将该用户添加到您的组织。


## 支持身份和访问权的服务访问策略
{: #iammanidaccser}

要管理用户的服务策略或为用户分配新的服务策略，您必须是帐户访问权管理员，或者必须分配为特定服务或服务实例的管理员。有关服务策略和角色的更多信息，请参阅[身份和访问权管理策略与角色](/docs/iam/users_roles.html#iamusermanpol)。有关用于管理策略的 CLI 命令的详细信息，请参阅[用于管理 API 密钥和策略的命令](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam)。

### 编辑现有策略

1. 在菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权** &gt; **用户**。
2. 选择要为其分配服务策略的用户名。
3. 从要编辑的策略所在的行中，选择**操作**菜单，然后单击**编辑策略**。
4. 编辑策略。
5. 单击**保存策略**。

### 添加新策略

1. 在菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权** &gt; **用户**。
2. 选择要为其分配服务策略的用户名。
3. 选择**分配策略**。
4. 选择服务。
5. 选择**所有当前区域**或特定区域（如果系统提示选择）。**注**：并非所有服务都需要选择区域。
6. 选择**所有当前服务实例**或选择特定服务实例。
7. 根据所选择的服务，可能会看到以下字段。如果您未输入这些字段的值，那么会在服务实例级别而非存储区级别来分配策略。 
    * **资源类型**：输入**存储区**。
    * **资源**：输入存储区的名称。
8. 选择用于定义策略的访问权作用域的角色。
9. 可选：选择**添加角色**为策略指定其他角色。

### 除去策略

1. 在菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权** &gt; **用户**。
2. 选择要为其分配服务策略的用户名。
3. 从要除去的策略所在的行中，选择**操作**菜单，然后单击**除去策略**。
4. 复查要除去的用户策略详细信息，然后通过单击**除去策略**进行确认。
  

## 基础架构服务许可权

要分配或更新基础架构许可权，请单击**分配基础架构访问权**链接。
