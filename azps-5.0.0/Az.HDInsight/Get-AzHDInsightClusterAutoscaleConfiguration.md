---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115375"
---
# <span data-ttu-id="36b9d-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b9d-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="36b9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="36b9d-103">Obtém a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="36b9d-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="36b9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36b9d-104">SYNTAX</span></span>

### <span data-ttu-id="36b9d-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="36b9d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36b9d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b9d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36b9d-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36b9d-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36b9d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36b9d-108">DESCRIPTION</span></span>
<span data-ttu-id="36b9d-109">O cmdlet **Get-AzHDInsightClusterAutoscaleConfiguration** Obtém a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="36b9d-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="36b9d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36b9d-110">EXAMPLES</span></span>

### <span data-ttu-id="36b9d-111">Exemplo 1: obter a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="36b9d-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="36b9d-112">Esse comando obtém a configuração de autoescala do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="36b9d-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="36b9d-113">OS</span><span class="sxs-lookup"><span data-stu-id="36b9d-113">PARAMETERS</span></span>

### <span data-ttu-id="36b9d-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="36b9d-114">-ClusterName</span></span>
<span data-ttu-id="36b9d-115">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="36b9d-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="36b9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b9d-116">-DefaultProfile</span></span>
<span data-ttu-id="36b9d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36b9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b9d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b9d-118">-InputObject</span></span>
<span data-ttu-id="36b9d-119">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="36b9d-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="36b9d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b9d-120">-ResourceGroupName</span></span>
<span data-ttu-id="36b9d-121">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36b9d-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="36b9d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36b9d-122">-ResourceId</span></span>
<span data-ttu-id="36b9d-123">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="36b9d-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="36b9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b9d-124">CommonParameters</span></span>
<span data-ttu-id="36b9d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b9d-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36b9d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b9d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36b9d-127">INPUTS</span></span>

### <span data-ttu-id="36b9d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="36b9d-128">System.String</span></span>

### <span data-ttu-id="36b9d-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="36b9d-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="36b9d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36b9d-130">OUTPUTS</span></span>

### <span data-ttu-id="36b9d-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="36b9d-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="36b9d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36b9d-132">NOTES</span></span>

## <span data-ttu-id="36b9d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36b9d-133">RELATED LINKS</span></span>

<span data-ttu-id="36b9d-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="36b9d-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
