---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113726"
---
# <span data-ttu-id="db081-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="db081-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="db081-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db081-102">SYNOPSIS</span></span>
<span data-ttu-id="db081-103">Remove um administrador do Azure AD para instância gerenciada pelo SQL.</span><span class="sxs-lookup"><span data-stu-id="db081-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="db081-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db081-104">SYNTAX</span></span>

### <span data-ttu-id="db081-105">UseResourceGroupAndInstanceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db081-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db081-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db081-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db081-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db081-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db081-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="db081-108">DESCRIPTION</span></span>
<span data-ttu-id="db081-109">O cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** remove um administrador do Azure Active Directory (Azure AD) para a Instância Gerenciada do AzureSQL na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="db081-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="db081-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db081-110">EXAMPLES</span></span>

### <span data-ttu-id="db081-111">Exemplo 1: Remover um administrador</span><span class="sxs-lookup"><span data-stu-id="db081-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="db081-112">Esse comando remove o administrador do Azure AD para a instância gerenciada chamada ManagedInstanceName01 associada ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="db081-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="db081-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db081-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="db081-114">Esse comando remove o administrador do Azure AD do objeto de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="db081-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="db081-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db081-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="db081-116">Esse comando remove o administrador do Azure AD usando o identificador de recurso de instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="db081-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="db081-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db081-117">PARAMETERS</span></span>

### <span data-ttu-id="db081-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db081-118">-DefaultProfile</span></span>
<span data-ttu-id="db081-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db081-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db081-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="db081-120">-Force</span></span>
<span data-ttu-id="db081-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="db081-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="db081-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db081-122">-InputObject</span></span>
<span data-ttu-id="db081-123">O objeto de instância gerenciado a ser usado.</span><span class="sxs-lookup"><span data-stu-id="db081-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="db081-124">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="db081-124">-InstanceName</span></span>
<span data-ttu-id="db081-125">Nome da Instância Gerenciada do SQL.</span><span class="sxs-lookup"><span data-stu-id="db081-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="db081-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db081-126">-PassThru</span></span>
<span data-ttu-id="db081-127">Define se o administrador do AD removido deve retornar</span><span class="sxs-lookup"><span data-stu-id="db081-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="db081-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db081-128">-ResourceGroupName</span></span>
<span data-ttu-id="db081-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db081-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="db081-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db081-130">-ResourceId</span></span>
<span data-ttu-id="db081-131">A ID do recurso de instância a ser usada</span><span class="sxs-lookup"><span data-stu-id="db081-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="db081-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db081-132">-Confirm</span></span>
<span data-ttu-id="db081-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db081-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db081-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db081-134">-WhatIf</span></span>
<span data-ttu-id="db081-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db081-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db081-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db081-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db081-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db081-137">CommonParameters</span></span>
<span data-ttu-id="db081-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db081-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db081-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db081-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db081-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="db081-140">INPUTS</span></span>

### <span data-ttu-id="db081-141">System.String</span><span class="sxs-lookup"><span data-stu-id="db081-141">System.String</span></span>

## <span data-ttu-id="db081-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="db081-142">OUTPUTS</span></span>

### <span data-ttu-id="db081-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="db081-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="db081-144">Notas</span><span class="sxs-lookup"><span data-stu-id="db081-144">NOTES</span></span>

## <span data-ttu-id="db081-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db081-145">RELATED LINKS</span></span>

[<span data-ttu-id="db081-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="db081-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="db081-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="db081-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
