---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 3d1e5db009cc88cf4647586c4234d63ae42f0575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770804"
---
# <span data-ttu-id="db114-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="db114-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="db114-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db114-102">SYNOPSIS</span></span>
<span data-ttu-id="db114-103">Obtém as propriedades sobre o serviço HDInsight, como locais e capacidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="db114-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="db114-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db114-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db114-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db114-105">DESCRIPTION</span></span>
<span data-ttu-id="db114-106">O cmdlet **Get-AzHDInsightProperty** Obtém propriedades específicas do Azure HDInsight, como a lista de locais disponíveis, versões de cluster HDInsight e capacidade de computação disponível.</span><span class="sxs-lookup"><span data-stu-id="db114-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="db114-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db114-107">EXAMPLES</span></span>

### <span data-ttu-id="db114-108">Exemplo 1: obter as propriedades de um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="db114-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="db114-109">Esse comando obtém as propriedades de um serviço HDInsight do local East US 2.</span><span class="sxs-lookup"><span data-stu-id="db114-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="db114-110">OS</span><span class="sxs-lookup"><span data-stu-id="db114-110">PARAMETERS</span></span>

### <span data-ttu-id="db114-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db114-111">-DefaultProfile</span></span>
<span data-ttu-id="db114-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db114-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db114-113">-Local</span><span class="sxs-lookup"><span data-stu-id="db114-113">-Location</span></span>
<span data-ttu-id="db114-114">Especifica o local para o qual buscar as propriedades do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db114-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="db114-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db114-115">CommonParameters</span></span>
<span data-ttu-id="db114-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db114-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db114-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db114-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db114-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db114-118">INPUTS</span></span>

### <span data-ttu-id="db114-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db114-119">None</span></span>

## <span data-ttu-id="db114-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db114-120">OUTPUTS</span></span>

### <span data-ttu-id="db114-121">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="db114-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="db114-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db114-122">NOTES</span></span>

## <span data-ttu-id="db114-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db114-123">RELATED LINKS</span></span>
