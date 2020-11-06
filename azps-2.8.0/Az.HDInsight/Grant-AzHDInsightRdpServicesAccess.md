---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596361"
---
# <span data-ttu-id="de84d-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="de84d-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="de84d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de84d-102">SYNOPSIS</span></span>
<span data-ttu-id="de84d-103">Concede acesso RDP ao cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="de84d-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="de84d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de84d-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de84d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de84d-105">DESCRIPTION</span></span>
<span data-ttu-id="de84d-106">O cmdlet **Grant-AzHDInsightRdpServicesAccess** permite que o RDP (protocolo de área de trabalho remota) acesse um cluster HDInsight do Windows baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="de84d-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="de84d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de84d-107">EXAMPLES</span></span>

### <span data-ttu-id="de84d-108">Exemplo 1: conceder acesso RDP a um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="de84d-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="de84d-109">Esse comando concede acesso RDP ao cluster chamado de-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="de84d-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="de84d-110">OS</span><span class="sxs-lookup"><span data-stu-id="de84d-110">PARAMETERS</span></span>

### <span data-ttu-id="de84d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="de84d-111">-ClusterName</span></span>
<span data-ttu-id="de84d-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="de84d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="de84d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de84d-113">-DefaultProfile</span></span>
<span data-ttu-id="de84d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="de84d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de84d-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="de84d-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="de84d-116">Especifica a expiração, como um objeto **DateTime** , para acesso RDP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="de84d-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="de84d-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="de84d-117">-RdpCredential</span></span>
<span data-ttu-id="de84d-118">Especifica as credenciais de RDP para o cluster.</span><span class="sxs-lookup"><span data-stu-id="de84d-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="de84d-119">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="de84d-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="de84d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de84d-120">-ResourceGroupName</span></span>
<span data-ttu-id="de84d-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de84d-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="de84d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de84d-122">CommonParameters</span></span>
<span data-ttu-id="de84d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de84d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de84d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de84d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de84d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de84d-125">INPUTS</span></span>

### <span data-ttu-id="de84d-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de84d-126">None</span></span>

## <span data-ttu-id="de84d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de84d-127">OUTPUTS</span></span>

### <span data-ttu-id="de84d-128">System. void</span><span class="sxs-lookup"><span data-stu-id="de84d-128">System.Void</span></span>

## <span data-ttu-id="de84d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de84d-129">NOTES</span></span>

## <span data-ttu-id="de84d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de84d-130">RELATED LINKS</span></span>

[<span data-ttu-id="de84d-131">REVOKE-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="de84d-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


