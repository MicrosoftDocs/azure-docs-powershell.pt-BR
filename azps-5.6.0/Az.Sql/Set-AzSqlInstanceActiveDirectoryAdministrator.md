---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: a8c748e2d37dbb4759df27b56b37719bcbb2babf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901558"
---
# <span data-ttu-id="d67cf-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d67cf-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="d67cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d67cf-103">Provisiona um administrador do Azure AD para SQL Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d67cf-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="d67cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d67cf-104">SYNTAX</span></span>

### <span data-ttu-id="d67cf-105">UseResourceGroupAndInstanceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d67cf-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d67cf-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67cf-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d67cf-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d67cf-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d67cf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d67cf-108">DESCRIPTION</span></span>
<span data-ttu-id="d67cf-109">O cmdlet **Set-AzSqlInstanceActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para Instância Gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d67cf-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="d67cf-110">Você pode provisioná-lo apenas um administrador por vez.</span><span class="sxs-lookup"><span data-stu-id="d67cf-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="d67cf-111">Os seguintes membros do Azure AD podem ser provisionados como SQL administrador de Instância Gerenciada:</span><span class="sxs-lookup"><span data-stu-id="d67cf-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="d67cf-112">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="d67cf-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="d67cf-113">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="d67cf-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="d67cf-114">Grupos do Azure AD criados como grupos de segurança Membros importados de outros Azure ADs não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="d67cf-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="d67cf-115">Contas da Microsoft, como aquelas nos domínios Outlook.com, Hotmail.com ou Live.com, não são suportadas como administradores.</span><span class="sxs-lookup"><span data-stu-id="d67cf-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="d67cf-116">Outras contas de convidado, como aquelas nos domínios Gmail.com Yahoo.com, não são suportadas como administradores.</span><span class="sxs-lookup"><span data-stu-id="d67cf-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="d67cf-117">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="d67cf-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="d67cf-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d67cf-118">EXAMPLES</span></span>

### <span data-ttu-id="d67cf-119">Exemplo 1: Provisione um grupo de administradores para uma instância gerenciada associada ao grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d67cf-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="d67cf-120">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para a instância gerenciada chamada ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="d67cf-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="d67cf-121">Esse servidor está associado ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d67cf-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="d67cf-122">Exemplo 2: Provisionar um usuário de administrador usando o objeto de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="d67cf-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="d67cf-123">Esse comando provisiona um usuário do Azure AD como administrador do objeto de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d67cf-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="d67cf-124">Exemplo 3: Provisione um administrador usando o identificador de recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="d67cf-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="d67cf-125">Esse comando provisiona um usuário do Azure AD como administrador usando o identificador de recurso de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d67cf-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="d67cf-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d67cf-126">PARAMETERS</span></span>

### <span data-ttu-id="d67cf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67cf-127">-DefaultProfile</span></span>
<span data-ttu-id="d67cf-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d67cf-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67cf-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d67cf-129">-DisplayName</span></span>
<span data-ttu-id="d67cf-130">Especifica o nome de exibição do usuário ou grupo para quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="d67cf-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="d67cf-131">Esse nome de exibição deve existir no active directory associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d67cf-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="d67cf-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d67cf-132">-InputObject</span></span>
<span data-ttu-id="d67cf-133">O objeto de instância gerenciada a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d67cf-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d67cf-134">-InstanceName</span></span>
<span data-ttu-id="d67cf-135">SQL nome da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d67cf-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d67cf-136">-ObjectId</span></span>
<span data-ttu-id="d67cf-137">Especifica a ID do objeto do usuário ou grupo no Azure Active Directory para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="d67cf-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d67cf-138">-ResourceGroupName</span></span>
<span data-ttu-id="d67cf-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d67cf-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d67cf-140">-ResourceId</span></span>
<span data-ttu-id="d67cf-141">A id de recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="d67cf-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d67cf-142">-Confirm</span></span>
<span data-ttu-id="d67cf-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d67cf-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d67cf-144">-WhatIf</span></span>
<span data-ttu-id="d67cf-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d67cf-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d67cf-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d67cf-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67cf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67cf-147">CommonParameters</span></span>
<span data-ttu-id="d67cf-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67cf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67cf-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d67cf-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67cf-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d67cf-150">INPUTS</span></span>

### <span data-ttu-id="d67cf-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d67cf-151">System.String</span></span>

### <span data-ttu-id="d67cf-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d67cf-152">System.Guid</span></span>

## <span data-ttu-id="d67cf-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d67cf-153">OUTPUTS</span></span>

### <span data-ttu-id="d67cf-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="d67cf-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="d67cf-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="d67cf-155">NOTES</span></span>

## <span data-ttu-id="d67cf-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d67cf-156">RELATED LINKS</span></span>

[<span data-ttu-id="d67cf-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d67cf-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="d67cf-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d67cf-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
