---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943197"
---
# <span data-ttu-id="74b48-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="74b48-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="74b48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74b48-102">SYNOPSIS</span></span>
<span data-ttu-id="74b48-103">Remove um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="74b48-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="74b48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74b48-104">SYNTAX</span></span>

### <span data-ttu-id="74b48-105">RemoveIFGDefaultSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="74b48-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b48-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="74b48-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b48-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="74b48-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b48-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74b48-108">DESCRIPTION</span></span>
<span data-ttu-id="74b48-109">Esse comando Remove o grupo de failover de instância com o nome especificado, deixando todos os bancos de dados intactos.</span><span class="sxs-lookup"><span data-stu-id="74b48-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="74b48-110">O ponto de extremidade de escuta será cancelado do DNS.</span><span class="sxs-lookup"><span data-stu-id="74b48-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="74b48-111">A região primária do grupo de failover de instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="74b48-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="74b48-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74b48-112">EXAMPLES</span></span>

### <span data-ttu-id="74b48-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74b48-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="74b48-114">Remover um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="74b48-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="74b48-115">OS</span><span class="sxs-lookup"><span data-stu-id="74b48-115">PARAMETERS</span></span>

### <span data-ttu-id="74b48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b48-116">-DefaultProfile</span></span>
<span data-ttu-id="74b48-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74b48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b48-118">-Force</span><span class="sxs-lookup"><span data-stu-id="74b48-118">-Force</span></span>
<span data-ttu-id="74b48-119">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="74b48-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="74b48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74b48-120">-InputObject</span></span>
<span data-ttu-id="74b48-121">O objeto de grupo de failover de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="74b48-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="74b48-122">-Local</span><span class="sxs-lookup"><span data-stu-id="74b48-122">-Location</span></span>
<span data-ttu-id="74b48-123">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="74b48-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="74b48-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="74b48-124">-Name</span></span>
<span data-ttu-id="74b48-125">O nome do grupo de failover de instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="74b48-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="74b48-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74b48-126">-PassThru</span></span>
<span data-ttu-id="74b48-127">Especifica se a saída de execução do cmdlet será transcorrido.</span><span class="sxs-lookup"><span data-stu-id="74b48-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="74b48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b48-128">-ResourceGroupName</span></span>
<span data-ttu-id="74b48-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74b48-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="74b48-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74b48-130">-ResourceId</span></span>
<span data-ttu-id="74b48-131">A ID do recurso do grupo de failover de instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="74b48-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="74b48-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74b48-132">-Confirm</span></span>
<span data-ttu-id="74b48-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b48-134">-WhatIf</span></span>
<span data-ttu-id="74b48-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74b48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b48-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74b48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b48-137">CommonParameters</span></span>
<span data-ttu-id="74b48-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b48-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74b48-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b48-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74b48-140">INPUTS</span></span>

### <span data-ttu-id="74b48-141">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="74b48-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="74b48-142">System. String</span><span class="sxs-lookup"><span data-stu-id="74b48-142">System.String</span></span>

## <span data-ttu-id="74b48-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74b48-143">OUTPUTS</span></span>

### <span data-ttu-id="74b48-144">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="74b48-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="74b48-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74b48-145">NOTES</span></span>

## <span data-ttu-id="74b48-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74b48-146">RELATED LINKS</span></span>
