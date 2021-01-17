---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: a4e02a10bef16fad21a44ca7952a5f2e429846d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426844"
---
# <span data-ttu-id="3f51d-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3f51d-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="3f51d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f51d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f51d-103">Seleciona um cluster para ser usado com o cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="3f51d-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="3f51d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f51d-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f51d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f51d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f51d-106">O cmdlet **use-AzHDInsightCluster** seleciona o cluster do Azure HDInsight para o cmdlet Invoke-AzHDInsightHiveJob usar para enviar trabalhos de Hive.</span><span class="sxs-lookup"><span data-stu-id="3f51d-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="3f51d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f51d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f51d-108">Exemplo 1: selecionar um cluster para envio de consulta de Hive</span><span class="sxs-lookup"><span data-stu-id="3f51d-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="3f51d-109">Esse comando seleciona um cluster para um envio de consulta de Hive.</span><span class="sxs-lookup"><span data-stu-id="3f51d-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="3f51d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3f51d-110">PARAMETERS</span></span>

### <span data-ttu-id="3f51d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f51d-111">-ClusterName</span></span>
<span data-ttu-id="3f51d-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3f51d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3f51d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f51d-113">-DefaultProfile</span></span>
<span data-ttu-id="3f51d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3f51d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f51d-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3f51d-115">-HttpCredential</span></span>
<span data-ttu-id="3f51d-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3f51d-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="3f51d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f51d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f51d-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f51d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3f51d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f51d-119">CommonParameters</span></span>
<span data-ttu-id="3f51d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f51d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f51d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f51d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f51d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f51d-122">INPUTS</span></span>

### <span data-ttu-id="3f51d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3f51d-123">None</span></span>

## <span data-ttu-id="3f51d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f51d-124">OUTPUTS</span></span>

### <span data-ttu-id="3f51d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3f51d-125">System.String</span></span>

## <span data-ttu-id="3f51d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f51d-126">NOTES</span></span>

## <span data-ttu-id="3f51d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f51d-127">RELATED LINKS</span></span>

[<span data-ttu-id="3f51d-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3f51d-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="3f51d-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3f51d-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


