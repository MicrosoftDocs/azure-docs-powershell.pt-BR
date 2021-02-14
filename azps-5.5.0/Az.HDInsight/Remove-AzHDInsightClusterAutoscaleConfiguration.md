---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116768"
---
# <span data-ttu-id="c19bc-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c19bc-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="c19bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c19bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c19bc-103">Remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c19bc-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="c19bc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c19bc-104">SYNTAX</span></span>

### <span data-ttu-id="c19bc-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c19bc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19bc-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19bc-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c19bc-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c19bc-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19bc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c19bc-108">DESCRIPTION</span></span>
<span data-ttu-id="c19bc-109">O cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c19bc-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="c19bc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c19bc-110">EXAMPLES</span></span>

### <span data-ttu-id="c19bc-111">Exemplo 1: Remover a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c19bc-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="c19bc-112">Esse comando remove a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c19bc-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="c19bc-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c19bc-113">PARAMETERS</span></span>

### <span data-ttu-id="c19bc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c19bc-114">-AsJob</span></span>
<span data-ttu-id="c19bc-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c19bc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c19bc-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c19bc-116">-ClusterName</span></span>
<span data-ttu-id="c19bc-117">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c19bc-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="c19bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c19bc-118">-DefaultProfile</span></span>
<span data-ttu-id="c19bc-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c19bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c19bc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c19bc-120">-InputObject</span></span>
<span data-ttu-id="c19bc-121">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="c19bc-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="c19bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="c19bc-123">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c19bc-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="c19bc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c19bc-124">-ResourceId</span></span>
<span data-ttu-id="c19bc-125">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c19bc-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="c19bc-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c19bc-126">-Confirm</span></span>
<span data-ttu-id="c19bc-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c19bc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19bc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19bc-128">-WhatIf</span></span>
<span data-ttu-id="c19bc-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c19bc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c19bc-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c19bc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19bc-131">CommonParameters</span></span>
<span data-ttu-id="c19bc-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c19bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19bc-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c19bc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19bc-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="c19bc-134">INPUTS</span></span>

### <span data-ttu-id="c19bc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c19bc-135">System.String</span></span>

### <span data-ttu-id="c19bc-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c19bc-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c19bc-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="c19bc-137">OUTPUTS</span></span>

### <span data-ttu-id="c19bc-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c19bc-138">System.Boolean</span></span>

## <span data-ttu-id="c19bc-139">Notas</span><span class="sxs-lookup"><span data-stu-id="c19bc-139">NOTES</span></span>

## <span data-ttu-id="c19bc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c19bc-140">RELATED LINKS</span></span>

<span data-ttu-id="c19bc-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c19bc-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
