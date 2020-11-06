---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427926"
---
# <span data-ttu-id="a2376-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a2376-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="a2376-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2376-102">SYNOPSIS</span></span>
<span data-ttu-id="a2376-103">Desabilita o acesso do RDP a um cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="a2376-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2376-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2376-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2376-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a2376-105">DESCRIPTION</span></span>
<span data-ttu-id="a2376-106">O cmdlet **REVOKE-AzureRmHDInsightRdpServicesAccess** desabilita o acesso do protocolo RDP a um cluster do Azure HDInsight baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="a2376-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a2376-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2376-107">EXAMPLES</span></span>

### <span data-ttu-id="a2376-108">Exemplo 1: desabilitar o acesso ao RDP para um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="a2376-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a2376-109">Esse comando revoga o acesso do RDP para o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a2376-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a2376-110">OS</span><span class="sxs-lookup"><span data-stu-id="a2376-110">PARAMETERS</span></span>

### <span data-ttu-id="a2376-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a2376-111">-ClusterName</span></span>
<span data-ttu-id="a2376-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a2376-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a2376-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2376-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2376-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a2376-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a2376-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2376-115">-DefaultProfile</span></span>
<span data-ttu-id="a2376-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2376-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2376-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2376-117">CommonParameters</span></span>
<span data-ttu-id="a2376-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2376-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2376-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2376-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2376-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a2376-120">INPUTS</span></span>

## <span data-ttu-id="a2376-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a2376-121">OUTPUTS</span></span>

### <span data-ttu-id="a2376-122">System. void</span><span class="sxs-lookup"><span data-stu-id="a2376-122">System.Void</span></span>

## <span data-ttu-id="a2376-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a2376-123">NOTES</span></span>

## <span data-ttu-id="a2376-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2376-124">RELATED LINKS</span></span>

[<span data-ttu-id="a2376-125">Grant AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a2376-125">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


