---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: c9b95a1f16c90eb3c6e057707dbf63d431b9a1ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893346"
---
# <span data-ttu-id="73848-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="73848-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="73848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73848-102">SYNOPSIS</span></span>
<span data-ttu-id="73848-103">Seleciona um cluster a ser usado com o Invoke-RmAzureHDInsightHiveJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73848-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="73848-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73848-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73848-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73848-105">DESCRIPTION</span></span>
<span data-ttu-id="73848-106">O cmdlet **Use-AzHDInsightCluster** seleciona o cluster HDInsight do Azure para o cmdlet Invoke-AzHDInsightHiveJob a ser usado para enviar trabalhos hive.</span><span class="sxs-lookup"><span data-stu-id="73848-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="73848-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73848-107">EXAMPLES</span></span>

### <span data-ttu-id="73848-108">Exemplo 1: Selecione um cluster para envio de consulta hive</span><span class="sxs-lookup"><span data-stu-id="73848-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="73848-109">Este comando seleciona um cluster para um envio de consulta hive.</span><span class="sxs-lookup"><span data-stu-id="73848-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="73848-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73848-110">PARAMETERS</span></span>

### <span data-ttu-id="73848-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="73848-111">-ClusterName</span></span>
<span data-ttu-id="73848-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="73848-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73848-113">-DefaultProfile</span></span>
<span data-ttu-id="73848-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="73848-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73848-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="73848-115">-HttpCredential</span></span>
<span data-ttu-id="73848-116">Especifica as credenciais de logon de cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="73848-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73848-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73848-117">-ResourceGroupName</span></span>
<span data-ttu-id="73848-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73848-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73848-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73848-119">CommonParameters</span></span>
<span data-ttu-id="73848-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73848-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73848-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73848-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73848-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73848-122">INPUTS</span></span>

### <span data-ttu-id="73848-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73848-123">None</span></span>

## <span data-ttu-id="73848-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73848-124">OUTPUTS</span></span>

### <span data-ttu-id="73848-125">System.String</span><span class="sxs-lookup"><span data-stu-id="73848-125">System.String</span></span>

## <span data-ttu-id="73848-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="73848-126">NOTES</span></span>

## <span data-ttu-id="73848-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73848-127">RELATED LINKS</span></span>

[<span data-ttu-id="73848-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="73848-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="73848-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="73848-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


