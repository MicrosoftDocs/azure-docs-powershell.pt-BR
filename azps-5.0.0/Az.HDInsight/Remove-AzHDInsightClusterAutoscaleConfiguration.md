---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117831"
---
# <span data-ttu-id="b502d-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b502d-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="b502d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b502d-102">SYNOPSIS</span></span>
<span data-ttu-id="b502d-103">Remove a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b502d-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b502d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b502d-104">SYNTAX</span></span>

### <span data-ttu-id="b502d-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b502d-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b502d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b502d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b502d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b502d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b502d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b502d-108">DESCRIPTION</span></span>
<span data-ttu-id="b502d-109">O cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** remove a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b502d-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b502d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b502d-110">EXAMPLES</span></span>

### <span data-ttu-id="b502d-111">Exemplo 1: remover a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b502d-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="b502d-112">Esse comando Remove a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b502d-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b502d-113">OS</span><span class="sxs-lookup"><span data-stu-id="b502d-113">PARAMETERS</span></span>

### <span data-ttu-id="b502d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b502d-114">-AsJob</span></span>
<span data-ttu-id="b502d-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b502d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b502d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b502d-116">-ClusterName</span></span>
<span data-ttu-id="b502d-117">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="b502d-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b502d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b502d-118">-DefaultProfile</span></span>
<span data-ttu-id="b502d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b502d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b502d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b502d-120">-InputObject</span></span>
<span data-ttu-id="b502d-121">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b502d-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b502d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b502d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b502d-123">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b502d-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b502d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b502d-124">-ResourceId</span></span>
<span data-ttu-id="b502d-125">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b502d-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b502d-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b502d-126">-Confirm</span></span>
<span data-ttu-id="b502d-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b502d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b502d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b502d-128">-WhatIf</span></span>
<span data-ttu-id="b502d-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b502d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b502d-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b502d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b502d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b502d-131">CommonParameters</span></span>
<span data-ttu-id="b502d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b502d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b502d-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b502d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b502d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b502d-134">INPUTS</span></span>

### <span data-ttu-id="b502d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b502d-135">System.String</span></span>

### <span data-ttu-id="b502d-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b502d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="b502d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b502d-137">OUTPUTS</span></span>

### <span data-ttu-id="b502d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b502d-138">System.Boolean</span></span>

## <span data-ttu-id="b502d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b502d-139">NOTES</span></span>

## <span data-ttu-id="b502d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b502d-140">RELATED LINKS</span></span>

<span data-ttu-id="b502d-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b502d-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
