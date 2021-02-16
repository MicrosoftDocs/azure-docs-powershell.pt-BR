---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118473"
---
# <span data-ttu-id="e4943-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4943-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="e4943-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4943-102">SYNOPSIS</span></span>
<span data-ttu-id="e4943-103">Obtém a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4943-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="e4943-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4943-104">SYNTAX</span></span>

### <span data-ttu-id="e4943-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4943-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4943-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4943-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4943-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4943-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4943-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4943-108">DESCRIPTION</span></span>
<span data-ttu-id="e4943-109">O cmdlet **Get-AzHDInsightClusterAutoscaleConfiguration** obtém a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4943-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="e4943-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4943-110">EXAMPLES</span></span>

### <span data-ttu-id="e4943-111">Exemplo 1: Obter a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4943-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="e4943-112">Esse comando obtém a configuração de escala automática do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e4943-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="e4943-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4943-113">PARAMETERS</span></span>

### <span data-ttu-id="e4943-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e4943-114">-ClusterName</span></span>
<span data-ttu-id="e4943-115">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e4943-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4943-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4943-116">-DefaultProfile</span></span>
<span data-ttu-id="e4943-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4943-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4943-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4943-118">-InputObject</span></span>
<span data-ttu-id="e4943-119">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e4943-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4943-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4943-120">-ResourceGroupName</span></span>
<span data-ttu-id="e4943-121">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4943-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4943-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4943-122">-ResourceId</span></span>
<span data-ttu-id="e4943-123">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e4943-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4943-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4943-124">CommonParameters</span></span>
<span data-ttu-id="e4943-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4943-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4943-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4943-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4943-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4943-127">INPUTS</span></span>

### <span data-ttu-id="e4943-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e4943-128">System.String</span></span>

### <span data-ttu-id="e4943-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e4943-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e4943-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4943-130">OUTPUTS</span></span>

### <span data-ttu-id="e4943-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="e4943-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="e4943-132">Notas</span><span class="sxs-lookup"><span data-stu-id="e4943-132">NOTES</span></span>

## <span data-ttu-id="e4943-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4943-133">RELATED LINKS</span></span>

<span data-ttu-id="e4943-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e4943-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
