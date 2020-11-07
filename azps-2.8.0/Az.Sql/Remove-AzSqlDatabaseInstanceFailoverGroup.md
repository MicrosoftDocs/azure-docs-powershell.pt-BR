---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773819"
---
# <span data-ttu-id="1fff7-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1fff7-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="1fff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fff7-102">SYNOPSIS</span></span>
<span data-ttu-id="1fff7-103">Remove um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="1fff7-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="1fff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fff7-104">SYNTAX</span></span>

### <span data-ttu-id="1fff7-105">RemoveIFGDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fff7-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fff7-106">Remover um grupo de failover de instância da ID do recurso</span><span class="sxs-lookup"><span data-stu-id="1fff7-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fff7-107">Remover um grupo de failover de instância da definição de instância AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1fff7-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fff7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fff7-108">DESCRIPTION</span></span>
<span data-ttu-id="1fff7-109">Esse comando Remove o grupo de failover de instância com o nome especificado, deixando todos os bancos de dados intactos.</span><span class="sxs-lookup"><span data-stu-id="1fff7-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="1fff7-110">O ponto de extremidade de escuta será cancelado do DNS.</span><span class="sxs-lookup"><span data-stu-id="1fff7-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="1fff7-111">A região primária do grupo de failover de instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="1fff7-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="1fff7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fff7-112">EXAMPLES</span></span>

### <span data-ttu-id="1fff7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fff7-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="1fff7-114">Remover um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="1fff7-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="1fff7-115">OS</span><span class="sxs-lookup"><span data-stu-id="1fff7-115">PARAMETERS</span></span>

### <span data-ttu-id="1fff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fff7-116">-DefaultProfile</span></span>
<span data-ttu-id="1fff7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fff7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1fff7-118">-Force</span></span>
<span data-ttu-id="1fff7-119">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="1fff7-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fff7-120">-InputObject</span></span>
<span data-ttu-id="1fff7-121">O objeto de grupo de failover de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="1fff7-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-122">-Local</span><span class="sxs-lookup"><span data-stu-id="1fff7-122">-Location</span></span>
<span data-ttu-id="1fff7-123">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="1fff7-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fff7-124">-Name</span></span>
<span data-ttu-id="1fff7-125">O nome do grupo de failover de instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1fff7-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fff7-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fff7-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fff7-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fff7-128">-ResourceId</span></span>
<span data-ttu-id="1fff7-129">A ID do recurso do grupo de failover de instância a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1fff7-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1fff7-130">-Confirm</span></span>
<span data-ttu-id="1fff7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fff7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fff7-132">-WhatIf</span></span>
<span data-ttu-id="1fff7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fff7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fff7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fff7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fff7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fff7-135">CommonParameters</span></span>
<span data-ttu-id="1fff7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fff7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fff7-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fff7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fff7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fff7-138">INPUTS</span></span>

### <span data-ttu-id="1fff7-139">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1fff7-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="1fff7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1fff7-140">System.String</span></span>

## <span data-ttu-id="1fff7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fff7-141">OUTPUTS</span></span>

### <span data-ttu-id="1fff7-142">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1fff7-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="1fff7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fff7-143">NOTES</span></span>

## <span data-ttu-id="1fff7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fff7-144">RELATED LINKS</span></span>
