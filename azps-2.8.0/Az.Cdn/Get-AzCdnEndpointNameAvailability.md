---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: f21c8303f1ec156132653a5d05c1149ef10a9ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597610"
---
# <span data-ttu-id="2b3c9-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2b3c9-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="2b3c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3c9-103">Obtém o status de disponibilidade do ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="2b3c9-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="2b3c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b3c9-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3c9-106">O cmdlet **Get-AzCdnEndpointNameAvailability** Obtém o status de disponibilidade do ponto de extremidade da rede de distribuição de conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3c9-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2b3c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b3c9-107">EXAMPLES</span></span>

## <span data-ttu-id="2b3c9-108">OS</span><span class="sxs-lookup"><span data-stu-id="2b3c9-108">PARAMETERS</span></span>

### <span data-ttu-id="2b3c9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3c9-109">-DefaultProfile</span></span>
<span data-ttu-id="2b3c9-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2b3c9-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b3c9-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2b3c9-111">-EndpointName</span></span>
<span data-ttu-id="2b3c9-112">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2b3c9-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2b3c9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3c9-113">CommonParameters</span></span>
<span data-ttu-id="2b3c9-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3c9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3c9-115">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b3c9-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3c9-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b3c9-116">INPUTS</span></span>

### <span data-ttu-id="2b3c9-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2b3c9-117">None</span></span>

## <span data-ttu-id="2b3c9-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b3c9-118">OUTPUTS</span></span>

### <span data-ttu-id="2b3c9-119">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="2b3c9-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="2b3c9-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b3c9-120">NOTES</span></span>

## <span data-ttu-id="2b3c9-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b3c9-121">RELATED LINKS</span></span>
