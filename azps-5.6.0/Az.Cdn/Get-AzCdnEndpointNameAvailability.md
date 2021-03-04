---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: daea57cb0e8c910fca4fedabad0e4583354c4072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887817"
---
# <span data-ttu-id="9fa07-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9fa07-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="9fa07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa07-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa07-103">Obtém o status de disponibilidade do ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="9fa07-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="9fa07-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9fa07-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa07-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9fa07-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa07-106">O cmdlet **Get-AzCdnEndpointNameAvailability** obtém o status de disponibilidade do ponto de extremidade cdn (Rede de Distribuição de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa07-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9fa07-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fa07-107">EXAMPLES</span></span>

## <span data-ttu-id="9fa07-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9fa07-108">PARAMETERS</span></span>

### <span data-ttu-id="9fa07-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa07-109">-DefaultProfile</span></span>
<span data-ttu-id="9fa07-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9fa07-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fa07-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9fa07-111">-EndpointName</span></span>
<span data-ttu-id="9fa07-112">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fa07-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa07-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa07-113">CommonParameters</span></span>
<span data-ttu-id="9fa07-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa07-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa07-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fa07-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa07-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fa07-116">INPUTS</span></span>

### <span data-ttu-id="9fa07-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9fa07-117">None</span></span>

## <span data-ttu-id="9fa07-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9fa07-118">OUTPUTS</span></span>

### <span data-ttu-id="9fa07-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="9fa07-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="9fa07-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="9fa07-120">NOTES</span></span>

## <span data-ttu-id="9fa07-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fa07-121">RELATED LINKS</span></span>
