---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: ce169dc1cce1552b48aa864885c6877624da0176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429542"
---
# <span data-ttu-id="12784-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12784-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="12784-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12784-102">SYNOPSIS</span></span>
<span data-ttu-id="12784-103">Concede acesso RDP ao cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="12784-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12784-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12784-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12784-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12784-105">DESCRIPTION</span></span>
<span data-ttu-id="12784-106">O cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** permite que o RDP (protocolo de área de trabalho remota) acesse um cluster HDInsight do Windows baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="12784-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="12784-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12784-107">EXAMPLES</span></span>

### <span data-ttu-id="12784-108">Exemplo 1: conceder acesso RDP a um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="12784-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="12784-109">Esse comando concede acesso RDP ao cluster chamado de-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="12784-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="12784-110">OS</span><span class="sxs-lookup"><span data-stu-id="12784-110">PARAMETERS</span></span>

### <span data-ttu-id="12784-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="12784-111">-ClusterName</span></span>
<span data-ttu-id="12784-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="12784-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="12784-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12784-113">-DefaultProfile</span></span>
<span data-ttu-id="12784-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12784-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12784-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="12784-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="12784-116">Especifica a expiração, como um objeto **DateTime** , para acesso RDP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="12784-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12784-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="12784-117">-RdpCredential</span></span>
<span data-ttu-id="12784-118">Especifica as credenciais de RDP para o cluster.</span><span class="sxs-lookup"><span data-stu-id="12784-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="12784-119">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="12784-119">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12784-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12784-120">-ResourceGroupName</span></span>
<span data-ttu-id="12784-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12784-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="12784-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12784-122">CommonParameters</span></span>
<span data-ttu-id="12784-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12784-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12784-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12784-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12784-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12784-125">INPUTS</span></span>

### <span data-ttu-id="12784-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12784-126">None</span></span>

## <span data-ttu-id="12784-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12784-127">OUTPUTS</span></span>

### <span data-ttu-id="12784-128">System. void</span><span class="sxs-lookup"><span data-stu-id="12784-128">System.Void</span></span>

## <span data-ttu-id="12784-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12784-129">NOTES</span></span>

## <span data-ttu-id="12784-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12784-130">RELATED LINKS</span></span>

[<span data-ttu-id="12784-131">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12784-131">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


