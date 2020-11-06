---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 8c3fd2340c1e15d5229a5fdfe9331b1d31c8c02a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440427"
---
# <span data-ttu-id="92acc-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="92acc-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="92acc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92acc-102">SYNOPSIS</span></span>
<span data-ttu-id="92acc-103">Desabilita o acesso do RDP a um cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="92acc-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92acc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92acc-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92acc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92acc-105">DESCRIPTION</span></span>
<span data-ttu-id="92acc-106">O cmdlet **REVOKE-AzureRmHDInsightRdpServicesAccess** desabilita o acesso do protocolo RDP a um cluster do Azure HDInsight baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="92acc-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="92acc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92acc-107">EXAMPLES</span></span>

### <span data-ttu-id="92acc-108">Exemplo 1: desabilitar o acesso ao RDP para um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="92acc-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="92acc-109">Esse comando revoga o acesso do RDP para o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="92acc-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="92acc-110">OS</span><span class="sxs-lookup"><span data-stu-id="92acc-110">PARAMETERS</span></span>

### <span data-ttu-id="92acc-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92acc-111">-ClusterName</span></span>
<span data-ttu-id="92acc-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="92acc-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="92acc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92acc-113">-DefaultProfile</span></span>
<span data-ttu-id="92acc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="92acc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92acc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92acc-115">-ResourceGroupName</span></span>
<span data-ttu-id="92acc-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92acc-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="92acc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92acc-117">CommonParameters</span></span>
<span data-ttu-id="92acc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92acc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92acc-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92acc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92acc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92acc-120">INPUTS</span></span>

### <span data-ttu-id="92acc-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="92acc-121">None</span></span>

## <span data-ttu-id="92acc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92acc-122">OUTPUTS</span></span>

### <span data-ttu-id="92acc-123">System. void</span><span class="sxs-lookup"><span data-stu-id="92acc-123">System.Void</span></span>

## <span data-ttu-id="92acc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92acc-124">NOTES</span></span>

## <span data-ttu-id="92acc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92acc-125">RELATED LINKS</span></span>

[<span data-ttu-id="92acc-126">Grant AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="92acc-126">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


