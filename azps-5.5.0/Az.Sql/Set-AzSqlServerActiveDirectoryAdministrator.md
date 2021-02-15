---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118930"
---
# <span data-ttu-id="699d6-101">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="699d6-101">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="699d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="699d6-102">SYNOPSIS</span></span>
<span data-ttu-id="699d6-103">Provisiona um administrador do Azure AD para SQL Server.</span><span class="sxs-lookup"><span data-stu-id="699d6-103">Provisions an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="699d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="699d6-104">SYNTAX</span></span>

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="699d6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="699d6-105">DESCRIPTION</span></span>
<span data-ttu-id="699d6-106">O cmdlet **Set-AzSqlServerActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para o AzureSQL Server na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="699d6-106">The **Set-AzSqlServerActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>
<span data-ttu-id="699d6-107">Você pode provisioná-lo apenas um administrador por vez.</span><span class="sxs-lookup"><span data-stu-id="699d6-107">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="699d6-108">Os seguintes membros do Azure AD podem ser provisionados como administradores do SQL Server:</span><span class="sxs-lookup"><span data-stu-id="699d6-108">The following members of Azure AD can be provisioned as a SQL Server administrator:</span></span>
- <span data-ttu-id="699d6-109">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="699d6-109">Native members of Azure AD</span></span> 
- <span data-ttu-id="699d6-110">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="699d6-110">Federated members of Azure AD</span></span> 
- <span data-ttu-id="699d6-111">Membros importados de outros Azure ADs que são membros nativos ou federados</span><span class="sxs-lookup"><span data-stu-id="699d6-111">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="699d6-112">Grupos do Azure AD criados como grupos de segurança contas da Microsoft, como as dos domínios Outlook.com, Hotmail.com ou Live.com, não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="699d6-112">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="699d6-113">Outras contas de convidado, como as dos domínios Gmail.com ou Yahoo.com, não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="699d6-113">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="699d6-114">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="699d6-114">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="699d6-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="699d6-115">EXAMPLES</span></span>

### <span data-ttu-id="699d6-116">Exemplo 1: Provisione um grupo de administradores para um servidor</span><span class="sxs-lookup"><span data-stu-id="699d6-116">Example 1: Provision an administrator group for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="699d6-117">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="699d6-117">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="699d6-118">Este servidor está associado ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="699d6-118">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="699d6-119">Exemplo 2: Provisione um usuário de administrador para um servidor</span><span class="sxs-lookup"><span data-stu-id="699d6-119">Example 2: Provision an administrator user for a server</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

<span data-ttu-id="699d6-120">Esse comando provisiona um usuário do Azure AD como administrador do servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="699d6-120">This command provisions an Azure AD user as an administrator for the server named Server01.</span></span>

### <span data-ttu-id="699d6-121">Exemplo 3: Provisionar um grupo de administradores especificando sua ID</span><span class="sxs-lookup"><span data-stu-id="699d6-121">Example 3: Provision an administrator group by specifying its ID</span></span>
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="699d6-122">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.</span><span class="sxs-lookup"><span data-stu-id="699d6-122">This command provisions an Azure AD administrator group named DBAs for the server named Server01.</span></span>
<span data-ttu-id="699d6-123">O comando especifica uma ID para o parâmetro *ObjectId.*</span><span class="sxs-lookup"><span data-stu-id="699d6-123">The command specifies an ID for the *ObjectId* parameter.</span></span>
<span data-ttu-id="699d6-124">Isso garante que o comando seja bem-sucedido mesmo que o nome de exibição do grupo não seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="699d6-124">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="699d6-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="699d6-125">PARAMETERS</span></span>

### <span data-ttu-id="699d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699d6-126">-DefaultProfile</span></span>
<span data-ttu-id="699d6-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="699d6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="699d6-128">-DisplayName</span></span>
<span data-ttu-id="699d6-129">Especifica o nome de exibição do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="699d6-129">Specifies the display name of the Azure AD administrator that this cmdlet provisions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="699d6-130">-ObjectId</span></span>
<span data-ttu-id="699d6-131">Especifica a ID exclusiva do administrador do Azure AD que este cmdlet provisiona.</span><span class="sxs-lookup"><span data-stu-id="699d6-131">Specifies the unique ID of the Azure AD administrator that this cmdlet provisions.</span></span>
<span data-ttu-id="699d6-132">Se o nome de exibição não for exclusivo, você deverá especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="699d6-132">If the display name is not unique, you must specify a value for this parameter.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699d6-133">-ResourceGroupName</span></span>
<span data-ttu-id="699d6-134">Especifica o nome do grupo de recursos ao qual o servidor é atribuído.</span><span class="sxs-lookup"><span data-stu-id="699d6-134">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="699d6-135">-ServerName</span></span>
<span data-ttu-id="699d6-136">Especifica o nome do SQL Server para o qual este cmdlet provisiona um administrador.</span><span class="sxs-lookup"><span data-stu-id="699d6-136">Specifies the name of the SQL Server for which this cmdlet provisions an administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="699d6-137">-Confirm</span></span>
<span data-ttu-id="699d6-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="699d6-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699d6-139">-WhatIf</span></span>
<span data-ttu-id="699d6-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="699d6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="699d6-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="699d6-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699d6-142">CommonParameters</span></span>
<span data-ttu-id="699d6-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699d6-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="699d6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699d6-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="699d6-145">INPUTS</span></span>

### <span data-ttu-id="699d6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="699d6-146">System.String</span></span>

### <span data-ttu-id="699d6-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="699d6-147">System.Guid</span></span>

## <span data-ttu-id="699d6-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="699d6-148">OUTPUTS</span></span>

### <span data-ttu-id="699d6-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="699d6-149">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="699d6-150">Notas</span><span class="sxs-lookup"><span data-stu-id="699d6-150">NOTES</span></span>

## <span data-ttu-id="699d6-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="699d6-151">RELATED LINKS</span></span>

[<span data-ttu-id="699d6-152">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="699d6-152">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="699d6-153">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="699d6-153">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="699d6-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="699d6-154">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="699d6-155">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="699d6-155">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


