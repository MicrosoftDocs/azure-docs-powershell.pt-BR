---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: e864e963e91df9599642c763a151325dd68d65a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889671"
---
# <span data-ttu-id="701ef-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="701ef-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="701ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="701ef-102">SYNOPSIS</span></span>
<span data-ttu-id="701ef-103">Define as credenciais HTTP do gateway de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="701ef-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="701ef-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="701ef-104">SYNTAX</span></span>

### <span data-ttu-id="701ef-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="701ef-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="701ef-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="701ef-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="701ef-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="701ef-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="701ef-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="701ef-108">DESCRIPTION</span></span>
<span data-ttu-id="701ef-109">O cmdlet **Set-AzHDInsightGatewayCredential** define a credencial de gateway de um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="701ef-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="701ef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="701ef-110">EXAMPLES</span></span>

### <span data-ttu-id="701ef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="701ef-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="701ef-112">Este comando define a credencial de gateway do cluster chamado seu-hadoop-001 por conjunto de parâmetros de nome.</span><span class="sxs-lookup"><span data-stu-id="701ef-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="701ef-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="701ef-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="701ef-114">Este comando define a credencial de gateway do cluster chamado your-hadoop-001 pelo conjunto de parâmetros ResourceId.</span><span class="sxs-lookup"><span data-stu-id="701ef-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="701ef-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="701ef-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="701ef-116">Este comando define a credencial de gateway do cluster chamado your-hadoop-001 pelo conjunto de parâmetros InputObject.</span><span class="sxs-lookup"><span data-stu-id="701ef-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="701ef-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="701ef-117">PARAMETERS</span></span>

### <span data-ttu-id="701ef-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="701ef-118">-AsJob</span></span>
<span data-ttu-id="701ef-119">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="701ef-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="701ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="701ef-120">-DefaultProfile</span></span>
<span data-ttu-id="701ef-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="701ef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="701ef-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="701ef-122">-HttpCredential</span></span>
<span data-ttu-id="701ef-123">Obtém ou define o logon do usuário do cluster.</span><span class="sxs-lookup"><span data-stu-id="701ef-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="701ef-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="701ef-124">-InputObject</span></span>
<span data-ttu-id="701ef-125">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="701ef-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="701ef-126">-Name</span><span class="sxs-lookup"><span data-stu-id="701ef-126">-Name</span></span>
<span data-ttu-id="701ef-127">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="701ef-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="701ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="701ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="701ef-129">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="701ef-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="701ef-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="701ef-130">-ResourceId</span></span>
<span data-ttu-id="701ef-131">Obtém ou define a id do recurso.</span><span class="sxs-lookup"><span data-stu-id="701ef-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="701ef-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="701ef-132">-Confirm</span></span>
<span data-ttu-id="701ef-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="701ef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="701ef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="701ef-134">-WhatIf</span></span>
<span data-ttu-id="701ef-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="701ef-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="701ef-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="701ef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="701ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="701ef-137">CommonParameters</span></span>
<span data-ttu-id="701ef-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="701ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="701ef-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="701ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="701ef-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="701ef-140">INPUTS</span></span>

### <span data-ttu-id="701ef-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="701ef-141">None</span></span>

## <span data-ttu-id="701ef-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="701ef-142">OUTPUTS</span></span>

### <span data-ttu-id="701ef-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="701ef-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="701ef-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="701ef-144">NOTES</span></span>

## <span data-ttu-id="701ef-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="701ef-145">RELATED LINKS</span></span>
