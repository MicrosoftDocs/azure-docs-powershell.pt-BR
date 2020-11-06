---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428210"
---
# <span data-ttu-id="e9ea3-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9ea3-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="e9ea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ea3-103">Concede acesso HTTP ao cluster.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9ea3-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9ea3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ea3-106">O cmdlet **Grant-AzureRmHDInsightHttpServicesAccess** concede acesso http a um cluster do Azure HDINSIGHT usando ODBC, Ambari, Oozie e Web Services.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="e9ea3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ea3-108">Exemplo 1: conceder acesso HTTP a um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e9ea3-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="e9ea3-109">Esse comando concede acesso HTTP ao cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e9ea3-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="e9ea3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e9ea3-111">-ClusterName</span></span>
<span data-ttu-id="e9ea3-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e9ea3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ea3-113">-DefaultProfile</span></span>
<span data-ttu-id="e9ea3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e9ea3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9ea3-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e9ea3-115">-HttpCredential</span></span>
<span data-ttu-id="e9ea3-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="e9ea3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ea3-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9ea3-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e9ea3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ea3-119">CommonParameters</span></span>
<span data-ttu-id="e9ea3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ea3-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ea3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ea3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9ea3-122">INPUTS</span></span>

### <span data-ttu-id="e9ea3-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e9ea3-123">None</span></span>
<span data-ttu-id="e9ea3-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e9ea3-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9ea3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9ea3-125">OUTPUTS</span></span>

### <span data-ttu-id="e9ea3-126">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="e9ea3-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="e9ea3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9ea3-127">NOTES</span></span>

## <span data-ttu-id="e9ea3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9ea3-128">RELATED LINKS</span></span>

[<span data-ttu-id="e9ea3-129">REVOKE-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e9ea3-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


