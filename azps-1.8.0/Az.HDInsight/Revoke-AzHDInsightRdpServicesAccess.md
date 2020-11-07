---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770770"
---
# <span data-ttu-id="a7da4-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a7da4-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="a7da4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7da4-102">SYNOPSIS</span></span>
<span data-ttu-id="a7da4-103">Desabilita o acesso do RDP a um cluster do Windows.</span><span class="sxs-lookup"><span data-stu-id="a7da4-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="a7da4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7da4-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7da4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7da4-105">DESCRIPTION</span></span>
<span data-ttu-id="a7da4-106">O cmdlet **REVOKE-AzHDInsightRdpServicesAccess** desabilita o acesso do protocolo RDP a um cluster do Azure HDInsight baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="a7da4-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a7da4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7da4-107">EXAMPLES</span></span>

### <span data-ttu-id="a7da4-108">Exemplo 1: desabilitar o acesso ao RDP para um cluster especificado</span><span class="sxs-lookup"><span data-stu-id="a7da4-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a7da4-109">Esse comando revoga o acesso do RDP para o cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a7da4-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a7da4-110">OS</span><span class="sxs-lookup"><span data-stu-id="a7da4-110">PARAMETERS</span></span>

### <span data-ttu-id="a7da4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a7da4-111">-ClusterName</span></span>
<span data-ttu-id="a7da4-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a7da4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a7da4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7da4-113">-DefaultProfile</span></span>
<span data-ttu-id="a7da4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a7da4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7da4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7da4-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7da4-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7da4-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a7da4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7da4-117">CommonParameters</span></span>
<span data-ttu-id="a7da4-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7da4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7da4-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7da4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7da4-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7da4-120">INPUTS</span></span>

### <span data-ttu-id="a7da4-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a7da4-121">None</span></span>

## <span data-ttu-id="a7da4-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7da4-122">OUTPUTS</span></span>

### <span data-ttu-id="a7da4-123">System. void</span><span class="sxs-lookup"><span data-stu-id="a7da4-123">System.Void</span></span>

## <span data-ttu-id="a7da4-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7da4-124">NOTES</span></span>

## <span data-ttu-id="a7da4-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7da4-125">RELATED LINKS</span></span>

[<span data-ttu-id="a7da4-126">Grant AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a7da4-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


