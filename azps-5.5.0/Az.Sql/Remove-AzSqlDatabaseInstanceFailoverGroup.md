---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115728"
---
# <span data-ttu-id="78f93-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78f93-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="78f93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78f93-102">SYNOPSIS</span></span>
<span data-ttu-id="78f93-103">Remove um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="78f93-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="78f93-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78f93-104">SYNTAX</span></span>

### <span data-ttu-id="78f93-105">RemoveIFGDefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="78f93-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f93-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="78f93-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f93-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="78f93-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f93-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="78f93-108">DESCRIPTION</span></span>
<span data-ttu-id="78f93-109">Esse comando remove o Grupo de Failover de Instância com o nome especificado, deixando todos os bancos de dados intactos.</span><span class="sxs-lookup"><span data-stu-id="78f93-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="78f93-110">O ponto de extremidade do ouvinte será não registro do DNS.</span><span class="sxs-lookup"><span data-stu-id="78f93-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="78f93-111">A região primária do Grupo de Failover de Instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="78f93-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="78f93-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78f93-112">EXAMPLES</span></span>

### <span data-ttu-id="78f93-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78f93-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="78f93-114">Remover um Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="78f93-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="78f93-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78f93-115">PARAMETERS</span></span>

### <span data-ttu-id="78f93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f93-116">-DefaultProfile</span></span>
<span data-ttu-id="78f93-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78f93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f93-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="78f93-118">-Force</span></span>
<span data-ttu-id="78f93-119">Ignorar a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="78f93-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="78f93-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f93-120">-InputObject</span></span>
<span data-ttu-id="78f93-121">O objeto Grupo de Failover de Instância para remover</span><span class="sxs-lookup"><span data-stu-id="78f93-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="78f93-122">-Local</span><span class="sxs-lookup"><span data-stu-id="78f93-122">-Location</span></span>
<span data-ttu-id="78f93-123">O nome da Região Local a partir da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="78f93-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="78f93-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="78f93-124">-Name</span></span>
<span data-ttu-id="78f93-125">O nome do Grupo de Failover de Instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="78f93-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="78f93-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78f93-126">-PassThru</span></span>
<span data-ttu-id="78f93-127">Especifica se você deve passar pela saída de execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f93-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="78f93-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f93-128">-ResourceGroupName</span></span>
<span data-ttu-id="78f93-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78f93-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="78f93-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78f93-130">-ResourceId</span></span>
<span data-ttu-id="78f93-131">A ID do Recurso do Grupo de Failover de Instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="78f93-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="78f93-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78f93-132">-Confirm</span></span>
<span data-ttu-id="78f93-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f93-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f93-134">-WhatIf</span></span>
<span data-ttu-id="78f93-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78f93-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f93-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78f93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f93-137">CommonParameters</span></span>
<span data-ttu-id="78f93-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f93-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78f93-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f93-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="78f93-140">INPUTS</span></span>

### <span data-ttu-id="78f93-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="78f93-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="78f93-142">System.String</span><span class="sxs-lookup"><span data-stu-id="78f93-142">System.String</span></span>

## <span data-ttu-id="78f93-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="78f93-143">OUTPUTS</span></span>

### <span data-ttu-id="78f93-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="78f93-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="78f93-145">Notas</span><span class="sxs-lookup"><span data-stu-id="78f93-145">NOTES</span></span>

## <span data-ttu-id="78f93-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78f93-146">RELATED LINKS</span></span>
