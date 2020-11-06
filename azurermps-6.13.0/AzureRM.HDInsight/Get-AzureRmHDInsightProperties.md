---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 198f0db3cab8b2e0f6e8f9b466ac3e0027e4638c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430269"
---
# <span data-ttu-id="c1c9d-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="c1c9d-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="c1c9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c9d-103">Obtém as propriedades sobre o serviço HDInsight, como locais e capacidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c1c9d-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1c9d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1c9d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c9d-106">O cmdlet **Get-AzureRmHDInsightProperties** Obtém propriedades específicas do Azure HDInsight, como a lista de locais disponíveis, versões de cluster HDInsight e capacidade de computação disponível.</span><span class="sxs-lookup"><span data-stu-id="c1c9d-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="c1c9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1c9d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c9d-108">Exemplo 1: obter as propriedades de um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c1c9d-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="c1c9d-109">Esse comando obtém as propriedades de um serviço HDInsight do local East US 2.</span><span class="sxs-lookup"><span data-stu-id="c1c9d-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="c1c9d-110">OS</span><span class="sxs-lookup"><span data-stu-id="c1c9d-110">PARAMETERS</span></span>

### <span data-ttu-id="c1c9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c9d-111">-DefaultProfile</span></span>
<span data-ttu-id="c1c9d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c1c9d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c9d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="c1c9d-113">-Location</span></span>
<span data-ttu-id="c1c9d-114">Especifica o local para o qual buscar as propriedades do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c1c9d-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="c1c9d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c9d-115">CommonParameters</span></span>
<span data-ttu-id="c1c9d-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c9d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c9d-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c9d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c9d-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1c9d-118">INPUTS</span></span>

### <span data-ttu-id="c1c9d-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c1c9d-119">None</span></span>

## <span data-ttu-id="c1c9d-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1c9d-120">OUTPUTS</span></span>

### <span data-ttu-id="c1c9d-121">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="c1c9d-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="c1c9d-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1c9d-122">NOTES</span></span>

## <span data-ttu-id="c1c9d-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1c9d-123">RELATED LINKS</span></span>
