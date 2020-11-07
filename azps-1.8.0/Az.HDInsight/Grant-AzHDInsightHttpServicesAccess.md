---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770794"
---
# <span data-ttu-id="db502-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db502-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="db502-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db502-102">SYNOPSIS</span></span>
<span data-ttu-id="db502-103">Concede acesso HTTP ao cluster.</span><span class="sxs-lookup"><span data-stu-id="db502-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="db502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db502-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db502-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db502-105">DESCRIPTION</span></span>
<span data-ttu-id="db502-106">O cmdlet **Grant-AzHDInsightHttpServicesAccess** concede acesso http a um cluster do Azure HDINSIGHT usando ODBC, Ambari, Oozie e Web Services.</span><span class="sxs-lookup"><span data-stu-id="db502-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="db502-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db502-107">EXAMPLES</span></span>

### <span data-ttu-id="db502-108">Exemplo 1: conceder acesso HTTP a um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="db502-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="db502-109">Esse comando concede acesso HTTP ao cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="db502-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="db502-110">OS</span><span class="sxs-lookup"><span data-stu-id="db502-110">PARAMETERS</span></span>

### <span data-ttu-id="db502-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="db502-111">-ClusterName</span></span>
<span data-ttu-id="db502-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="db502-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="db502-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db502-113">-DefaultProfile</span></span>
<span data-ttu-id="db502-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db502-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db502-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="db502-115">-HttpCredential</span></span>
<span data-ttu-id="db502-116">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="db502-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="db502-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db502-117">-ResourceGroupName</span></span>
<span data-ttu-id="db502-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db502-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="db502-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db502-119">CommonParameters</span></span>
<span data-ttu-id="db502-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db502-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db502-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db502-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db502-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db502-122">INPUTS</span></span>

### <span data-ttu-id="db502-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db502-123">None</span></span>

## <span data-ttu-id="db502-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db502-124">OUTPUTS</span></span>

### <span data-ttu-id="db502-125">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="db502-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="db502-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db502-126">NOTES</span></span>

## <span data-ttu-id="db502-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db502-127">RELATED LINKS</span></span>

[<span data-ttu-id="db502-128">REVOKE-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="db502-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


