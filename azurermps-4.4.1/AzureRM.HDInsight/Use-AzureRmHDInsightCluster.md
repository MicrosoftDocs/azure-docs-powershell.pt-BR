---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610776"
---
# <span data-ttu-id="2a664-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2a664-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="2a664-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a664-102">SYNOPSIS</span></span>
<span data-ttu-id="2a664-103">Seleciona um cluster para ser usado com o cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="2a664-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a664-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a664-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a664-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a664-105">DESCRIPTION</span></span>
<span data-ttu-id="2a664-106">O cmdlet **use-AzureRmHDInsightCluster** seleciona o cluster do Azure HDInsight para o cmdlet Invoke-AzureRmHDInsightHiveJob usar para enviar trabalhos de Hive.</span><span class="sxs-lookup"><span data-stu-id="2a664-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="2a664-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a664-107">EXAMPLES</span></span>

### <span data-ttu-id="2a664-108">Exemplo 1: selecionar um cluster para envio de consulta de Hive</span><span class="sxs-lookup"><span data-stu-id="2a664-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2a664-109">Esse comando seleciona um cluster para um envio de consulta de Hive.</span><span class="sxs-lookup"><span data-stu-id="2a664-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="2a664-110">OS</span><span class="sxs-lookup"><span data-stu-id="2a664-110">PARAMETERS</span></span>

### <span data-ttu-id="2a664-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2a664-111">-ClusterName</span></span>
<span data-ttu-id="2a664-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2a664-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2a664-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="2a664-113">-HttpCredential</span></span>
<span data-ttu-id="2a664-114">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2a664-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2a664-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a664-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a664-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a664-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2a664-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a664-117">-DefaultProfile</span></span>
<span data-ttu-id="2a664-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a664-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a664-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a664-119">CommonParameters</span></span>
<span data-ttu-id="2a664-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a664-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a664-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a664-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a664-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a664-122">INPUTS</span></span>

## <span data-ttu-id="2a664-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a664-123">OUTPUTS</span></span>

### <span data-ttu-id="2a664-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2a664-124">System.String</span></span>

## <span data-ttu-id="2a664-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a664-125">NOTES</span></span>

## <span data-ttu-id="2a664-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a664-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a664-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2a664-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="2a664-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2a664-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


