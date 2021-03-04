---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 0e3bfc112ee8c80d08b0b5a87eb574a4c5bdb29e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886128"
---
# <span data-ttu-id="fb7c1-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fb7c1-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="fb7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7c1-103">Remove um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="fb7c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fb7c1-104">SYNTAX</span></span>

### <span data-ttu-id="fb7c1-105">RemoveIFGDefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb7c1-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7c1-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7c1-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7c1-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="fb7c1-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7c1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fb7c1-108">DESCRIPTION</span></span>
<span data-ttu-id="fb7c1-109">Este comando remove o Grupo de Failover de Instância com o nome especificado, deixando todos os bancos de dados intactos.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="fb7c1-110">O ponto de extremidade do ouvinte será não registro no DNS.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="fb7c1-111">A região principal do Grupo de Failover de Instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="fb7c1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-112">EXAMPLES</span></span>

### <span data-ttu-id="fb7c1-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb7c1-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="fb7c1-114">Remover um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="fb7c1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-115">PARAMETERS</span></span>

### <span data-ttu-id="fb7c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7c1-116">-DefaultProfile</span></span>
<span data-ttu-id="fb7c1-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7c1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb7c1-118">-Force</span></span>
<span data-ttu-id="fb7c1-119">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="fb7c1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7c1-120">-InputObject</span></span>
<span data-ttu-id="fb7c1-121">O objeto Do Grupo de Failover de Instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="fb7c1-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7c1-122">-Location</span><span class="sxs-lookup"><span data-stu-id="fb7c1-122">-Location</span></span>
<span data-ttu-id="fb7c1-123">O nome da Região Local da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7c1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fb7c1-124">-Name</span></span>
<span data-ttu-id="fb7c1-125">O nome do Grupo de Failover de Instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7c1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb7c1-126">-PassThru</span></span>
<span data-ttu-id="fb7c1-127">Especifica se a saída de execução do cmdlet deve ser aprovada.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="fb7c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb7c1-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb7c1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7c1-130">-ResourceId</span></span>
<span data-ttu-id="fb7c1-131">A ID de Recurso do Grupo de Failover de Instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb7c1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb7c1-132">-Confirm</span></span>
<span data-ttu-id="fb7c1-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7c1-134">-WhatIf</span></span>
<span data-ttu-id="fb7c1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7c1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7c1-137">CommonParameters</span></span>
<span data-ttu-id="fb7c1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7c1-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb7c1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7c1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-140">INPUTS</span></span>

### <span data-ttu-id="fb7c1-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="fb7c1-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="fb7c1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fb7c1-142">System.String</span></span>

## <span data-ttu-id="fb7c1-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-143">OUTPUTS</span></span>

### <span data-ttu-id="fb7c1-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="fb7c1-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="fb7c1-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="fb7c1-145">NOTES</span></span>

## <span data-ttu-id="fb7c1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb7c1-146">RELATED LINKS</span></span>
