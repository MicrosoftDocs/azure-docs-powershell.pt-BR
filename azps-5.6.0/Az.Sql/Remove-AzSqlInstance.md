---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885780"
---
# <span data-ttu-id="44d30-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44d30-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="44d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44d30-102">SYNOPSIS</span></span>
<span data-ttu-id="44d30-103">Remove uma instância de banco de dados gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="44d30-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="44d30-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44d30-104">SYNTAX</span></span>

### <span data-ttu-id="44d30-105">RemoveInstanceFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44d30-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44d30-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="44d30-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44d30-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="44d30-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44d30-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44d30-108">DESCRIPTION</span></span>
<span data-ttu-id="44d30-109">O cmdlet **Remove-AzSqlInstance** remove uma instância gerenciada do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="44d30-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="44d30-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44d30-110">EXAMPLES</span></span>

### <span data-ttu-id="44d30-111">Exemplo 1: Remover instância</span><span class="sxs-lookup"><span data-stu-id="44d30-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="44d30-112">Este comando remove a instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="44d30-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="44d30-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44d30-113">PARAMETERS</span></span>

### <span data-ttu-id="44d30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d30-114">-DefaultProfile</span></span>
<span data-ttu-id="44d30-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44d30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44d30-116">-Force</span><span class="sxs-lookup"><span data-stu-id="44d30-116">-Force</span></span>
<span data-ttu-id="44d30-117">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="44d30-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="44d30-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44d30-118">-InputObject</span></span>
<span data-ttu-id="44d30-119">O objeto AzureSqlManagedInstanceModel a ser removido</span><span class="sxs-lookup"><span data-stu-id="44d30-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44d30-120">-Name</span><span class="sxs-lookup"><span data-stu-id="44d30-120">-Name</span></span>
<span data-ttu-id="44d30-121">SQL nome da instância.</span><span class="sxs-lookup"><span data-stu-id="44d30-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d30-122">-ResourceGroupName</span></span>
<span data-ttu-id="44d30-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44d30-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d30-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44d30-124">-ResourceId</span></span>
<span data-ttu-id="44d30-125">A ID do recurso do objeto instance a ser removido</span><span class="sxs-lookup"><span data-stu-id="44d30-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d30-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44d30-126">-Confirm</span></span>
<span data-ttu-id="44d30-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44d30-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44d30-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44d30-128">-WhatIf</span></span>
<span data-ttu-id="44d30-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44d30-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44d30-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44d30-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44d30-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d30-131">CommonParameters</span></span>
<span data-ttu-id="44d30-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d30-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d30-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44d30-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d30-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44d30-134">INPUTS</span></span>

### <span data-ttu-id="44d30-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="44d30-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="44d30-136">System.String</span><span class="sxs-lookup"><span data-stu-id="44d30-136">System.String</span></span>

## <span data-ttu-id="44d30-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44d30-137">OUTPUTS</span></span>

### <span data-ttu-id="44d30-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="44d30-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="44d30-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="44d30-139">NOTES</span></span>

## <span data-ttu-id="44d30-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44d30-140">RELATED LINKS</span></span>
