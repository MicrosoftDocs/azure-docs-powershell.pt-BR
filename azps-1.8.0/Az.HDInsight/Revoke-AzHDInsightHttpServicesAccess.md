---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770771"
---
# <span data-ttu-id="12a6b-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12a6b-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="12a6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="12a6b-103">Desabilita o acesso HTTP ao cluster.</span><span class="sxs-lookup"><span data-stu-id="12a6b-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="12a6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12a6b-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12a6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="12a6b-106">O cmdlet **REVOKE-AzHDInsightHttpServicesAccess** desabilita o acesso http a um cluster do Azure HDInsight para os serviços Web ODBC, Ambari, Oozie e webHCatalog.</span><span class="sxs-lookup"><span data-stu-id="12a6b-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="12a6b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="12a6b-108">Exemplo 1: desabilitar o acesso HTTP a um cluster</span><span class="sxs-lookup"><span data-stu-id="12a6b-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="12a6b-109">Esse comando revoga o acesso HTTP ao cluster chamado seu hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="12a6b-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="12a6b-110">OS</span><span class="sxs-lookup"><span data-stu-id="12a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="12a6b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="12a6b-111">-ClusterName</span></span>
<span data-ttu-id="12a6b-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="12a6b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="12a6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a6b-113">-DefaultProfile</span></span>
<span data-ttu-id="12a6b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12a6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12a6b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a6b-115">-ResourceGroupName</span></span>
<span data-ttu-id="12a6b-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12a6b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="12a6b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a6b-117">CommonParameters</span></span>
<span data-ttu-id="12a6b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a6b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a6b-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a6b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a6b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12a6b-120">INPUTS</span></span>

### <span data-ttu-id="12a6b-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12a6b-121">None</span></span>

## <span data-ttu-id="12a6b-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12a6b-122">OUTPUTS</span></span>

### <span data-ttu-id="12a6b-123">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="12a6b-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="12a6b-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12a6b-124">NOTES</span></span>

## <span data-ttu-id="12a6b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12a6b-125">RELATED LINKS</span></span>

[<span data-ttu-id="12a6b-126">Grant AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="12a6b-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


