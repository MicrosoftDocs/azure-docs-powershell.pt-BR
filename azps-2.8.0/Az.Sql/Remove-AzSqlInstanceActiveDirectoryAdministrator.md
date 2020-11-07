---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: fc2a5b4c25804658ad30c5f3554688746bdde74a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773802"
---
# <span data-ttu-id="0d76c-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d76c-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="0d76c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d76c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d76c-103">Remove uma instância gerenciada do Azure AD Administrator para SQL.</span><span class="sxs-lookup"><span data-stu-id="0d76c-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="0d76c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d76c-104">SYNTAX</span></span>

### <span data-ttu-id="0d76c-105">UseResourceGroupAndInstanceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d76c-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d76c-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d76c-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d76c-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d76c-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d76c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d76c-108">DESCRIPTION</span></span>
<span data-ttu-id="0d76c-109">O cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para AzureSQL instância gerenciada na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0d76c-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="0d76c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d76c-110">EXAMPLES</span></span>

### <span data-ttu-id="0d76c-111">Exemplo 1: remover um administrador</span><span class="sxs-lookup"><span data-stu-id="0d76c-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0d76c-112">Esse comando Remove o administrador do Azure AD da instância gerenciada nomeada ManagedInstanceName01 associada à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d76c-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="0d76c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0d76c-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0d76c-114">Esse comando Remove o Azure AD Administrator do objeto de instância gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0d76c-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="0d76c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0d76c-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="0d76c-116">Esse comando Remove o administrador do Azure AD usando o identificador de recursos de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="0d76c-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="0d76c-117">OS</span><span class="sxs-lookup"><span data-stu-id="0d76c-117">PARAMETERS</span></span>

### <span data-ttu-id="0d76c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d76c-118">-DefaultProfile</span></span>
<span data-ttu-id="0d76c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d76c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d76c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0d76c-120">-Force</span></span>
<span data-ttu-id="0d76c-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="0d76c-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d76c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d76c-122">-InputObject</span></span>
<span data-ttu-id="0d76c-123">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0d76c-123">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d76c-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0d76c-124">-InstanceName</span></span>
<span data-ttu-id="0d76c-125">Nome da instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="0d76c-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="0d76c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d76c-126">-PassThru</span></span>
<span data-ttu-id="0d76c-127">Define se o administrador de AD removido deve ser retornado</span><span class="sxs-lookup"><span data-stu-id="0d76c-127">Defines whether to return the removed AD administrator</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d76c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d76c-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d76c-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d76c-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d76c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d76c-130">-ResourceId</span></span>
<span data-ttu-id="0d76c-131">A ID do recurso da instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="0d76c-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="0d76c-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d76c-132">-Confirm</span></span>
<span data-ttu-id="0d76c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d76c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d76c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d76c-134">-WhatIf</span></span>
<span data-ttu-id="0d76c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d76c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d76c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d76c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d76c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d76c-137">CommonParameters</span></span>
<span data-ttu-id="0d76c-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d76c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d76c-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d76c-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d76c-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d76c-140">INPUTS</span></span>

### <span data-ttu-id="0d76c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0d76c-141">System.String</span></span>

## <span data-ttu-id="0d76c-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d76c-142">OUTPUTS</span></span>

### <span data-ttu-id="0d76c-143">Microsoft. Azure. Commands. Sql. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="0d76c-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="0d76c-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d76c-144">NOTES</span></span>

## <span data-ttu-id="0d76c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d76c-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d76c-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d76c-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="0d76c-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0d76c-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
