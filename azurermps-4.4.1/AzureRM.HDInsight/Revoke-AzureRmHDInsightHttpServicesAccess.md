---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 795882aa421037252ca920093f1df39b4e242fce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427927"
---
# <span data-ttu-id="bfc36-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bfc36-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="bfc36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc36-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc36-103">Desabilita o acesso HTTP ao cluster.</span><span class="sxs-lookup"><span data-stu-id="bfc36-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfc36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfc36-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc36-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfc36-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc36-106">O cmdlet **REVOKE-AzureRmHDInsightHttpServicesAccess** desabilita o acesso http a um cluster do Azure HDInsight para os serviços Web ODBC, Ambari, Oozie e webHCatalog.</span><span class="sxs-lookup"><span data-stu-id="bfc36-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="bfc36-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc36-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc36-108">Exemplo 1: desabilitar o acesso HTTP a um cluster</span><span class="sxs-lookup"><span data-stu-id="bfc36-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="bfc36-109">Esse comando revoga o acesso HTTP ao cluster chamado seu hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="bfc36-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="bfc36-110">OS</span><span class="sxs-lookup"><span data-stu-id="bfc36-110">PARAMETERS</span></span>

### <span data-ttu-id="bfc36-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bfc36-111">-ClusterName</span></span>
<span data-ttu-id="bfc36-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bfc36-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bfc36-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc36-113">-ResourceGroupName</span></span>
<span data-ttu-id="bfc36-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bfc36-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bfc36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc36-115">-DefaultProfile</span></span>
<span data-ttu-id="bfc36-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc36-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc36-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc36-117">CommonParameters</span></span>
<span data-ttu-id="bfc36-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc36-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc36-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc36-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc36-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfc36-120">INPUTS</span></span>

## <span data-ttu-id="bfc36-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfc36-121">OUTPUTS</span></span>

### <span data-ttu-id="bfc36-122">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="bfc36-122">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="bfc36-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfc36-123">NOTES</span></span>

## <span data-ttu-id="bfc36-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc36-124">RELATED LINKS</span></span>

[<span data-ttu-id="bfc36-125">Grant AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bfc36-125">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


