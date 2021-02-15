---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112184"
---
# <span data-ttu-id="67ecc-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="67ecc-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="67ecc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="67ecc-103">Obtém o status de disponibilidade do ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="67ecc-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="67ecc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ecc-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67ecc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ecc-105">DESCRIPTION</span></span>
<span data-ttu-id="67ecc-106">O cmdlet **Get-AzCdnEndpointNameAvailability** obtém o status de disponibilidade do ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="67ecc-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="67ecc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67ecc-107">EXAMPLES</span></span>

## <span data-ttu-id="67ecc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ecc-108">PARAMETERS</span></span>

### <span data-ttu-id="67ecc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ecc-109">-DefaultProfile</span></span>
<span data-ttu-id="67ecc-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="67ecc-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67ecc-111">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="67ecc-111">-EndpointName</span></span>
<span data-ttu-id="67ecc-112">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="67ecc-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="67ecc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ecc-113">CommonParameters</span></span>
<span data-ttu-id="67ecc-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ecc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ecc-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ecc-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ecc-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="67ecc-116">INPUTS</span></span>

### <span data-ttu-id="67ecc-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="67ecc-117">None</span></span>

## <span data-ttu-id="67ecc-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="67ecc-118">OUTPUTS</span></span>

### <span data-ttu-id="67ecc-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="67ecc-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="67ecc-120">Notas</span><span class="sxs-lookup"><span data-stu-id="67ecc-120">NOTES</span></span>

## <span data-ttu-id="67ecc-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ecc-121">RELATED LINKS</span></span>
