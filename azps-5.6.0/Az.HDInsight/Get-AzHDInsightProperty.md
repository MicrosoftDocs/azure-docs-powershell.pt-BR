---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892788"
---
# <span data-ttu-id="c4cc0-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="c4cc0-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="c4cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cc0-103">Obtém propriedades sobre o serviço HDInsight, como locais disponíveis e capacidade.</span><span class="sxs-lookup"><span data-stu-id="c4cc0-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="c4cc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4cc0-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4cc0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cc0-106">O cmdlet **Get-AzHDInsightProperty** obtém propriedades específicas do Azure HDInsight, como a lista de locais disponíveis, versões de cluster HDInsight e capacidade de computação disponível.</span><span class="sxs-lookup"><span data-stu-id="c4cc0-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="c4cc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cc0-108">Exemplo 1: Obter as propriedades de um cluster HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="c4cc0-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="c4cc0-109">Este comando obtém propriedades de um serviço HDInsight do local Leste dos EUA 2.</span><span class="sxs-lookup"><span data-stu-id="c4cc0-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="c4cc0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="c4cc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cc0-111">-DefaultProfile</span></span>
<span data-ttu-id="c4cc0-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c4cc0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4cc0-113">-Location</span><span class="sxs-lookup"><span data-stu-id="c4cc0-113">-Location</span></span>
<span data-ttu-id="c4cc0-114">Especifica o local para o qual buscar propriedades HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4cc0-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="c4cc0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cc0-115">CommonParameters</span></span>
<span data-ttu-id="c4cc0-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4cc0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cc0-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4cc0-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cc0-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-118">INPUTS</span></span>

### <span data-ttu-id="c4cc0-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c4cc0-119">None</span></span>
## <span data-ttu-id="c4cc0-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-120">OUTPUTS</span></span>

### <span data-ttu-id="c4cc0-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="c4cc0-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="c4cc0-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4cc0-122">NOTES</span></span>

## <span data-ttu-id="c4cc0-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4cc0-123">RELATED LINKS</span></span>
