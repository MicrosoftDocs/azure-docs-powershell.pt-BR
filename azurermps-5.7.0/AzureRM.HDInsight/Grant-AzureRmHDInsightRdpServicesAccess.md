---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602372"
---
# <span data-ttu-id="18c8a-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="18c8a-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="18c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="18c8a-103">Concede acesso RDP ao cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="18c8a-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18c8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18c8a-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18c8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="18c8a-106">O cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** permite que o RDP (protocolo de área de trabalho remota) acesse um cluster HDInsight do Windows baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="18c8a-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="18c8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18c8a-107">EXAMPLES</span></span>

### <span data-ttu-id="18c8a-108">Exemplo 1: conceder acesso RDP a um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="18c8a-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="18c8a-109">Esse comando concede acesso RDP ao cluster chamado de-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="18c8a-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="18c8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="18c8a-110">PARAMETERS</span></span>

### <span data-ttu-id="18c8a-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="18c8a-111">-ClusterName</span></span>
<span data-ttu-id="18c8a-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="18c8a-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c8a-113">-DefaultProfile</span></span>
<span data-ttu-id="18c8a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="18c8a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18c8a-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="18c8a-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="18c8a-116">Especifica a expiração, como um objeto **DateTime** , para acesso RDP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="18c8a-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c8a-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="18c8a-117">-RdpCredential</span></span>
<span data-ttu-id="18c8a-118">Especifica as credenciais de RDP para o cluster.</span><span class="sxs-lookup"><span data-stu-id="18c8a-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="18c8a-119">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="18c8a-119">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="18c8a-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18c8a-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18c8a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c8a-122">CommonParameters</span></span>
<span data-ttu-id="18c8a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c8a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c8a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c8a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c8a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18c8a-125">INPUTS</span></span>

### <span data-ttu-id="18c8a-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="18c8a-126">None</span></span>
<span data-ttu-id="18c8a-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="18c8a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18c8a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18c8a-128">OUTPUTS</span></span>

### <span data-ttu-id="18c8a-129">System. void</span><span class="sxs-lookup"><span data-stu-id="18c8a-129">System.Void</span></span>

## <span data-ttu-id="18c8a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18c8a-130">NOTES</span></span>

## <span data-ttu-id="18c8a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18c8a-131">RELATED LINKS</span></span>

[<span data-ttu-id="18c8a-132">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="18c8a-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


