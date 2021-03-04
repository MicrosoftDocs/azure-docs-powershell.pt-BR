---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: afc2400feb8694e74dd46731969429d6d7784369
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892560"
---
# <span data-ttu-id="0b687-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="0b687-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="0b687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b687-102">SYNOPSIS</span></span>
<span data-ttu-id="0b687-103">Valida uma URL de sonda.</span><span class="sxs-lookup"><span data-stu-id="0b687-103">Validates a probe URL.</span></span>

## <span data-ttu-id="0b687-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b687-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b687-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b687-105">DESCRIPTION</span></span>
<span data-ttu-id="0b687-106">O cmdlet **Confirm-AzCdnEndpointProbeURL** confirma se a URL da sonda fornecida pode ser usada para aceleração dinâmica do site.</span><span class="sxs-lookup"><span data-stu-id="0b687-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="0b687-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b687-107">EXAMPLES</span></span>

### <span data-ttu-id="0b687-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b687-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="0b687-109">Valida a url da sonda " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="0b687-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="0b687-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b687-110">PARAMETERS</span></span>

### <span data-ttu-id="0b687-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b687-111">-DefaultProfile</span></span>
<span data-ttu-id="0b687-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b687-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b687-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="0b687-113">-ProbeUrl</span></span>
<span data-ttu-id="0b687-114">Nome da URL da sonda proposta para validar.</span><span class="sxs-lookup"><span data-stu-id="0b687-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="0b687-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b687-115">CommonParameters</span></span>
<span data-ttu-id="0b687-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b687-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b687-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b687-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b687-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b687-118">INPUTS</span></span>

### <span data-ttu-id="0b687-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0b687-119">None</span></span>

## <span data-ttu-id="0b687-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b687-120">OUTPUTS</span></span>

### <span data-ttu-id="0b687-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="0b687-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="0b687-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b687-122">NOTES</span></span>

## <span data-ttu-id="0b687-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b687-123">RELATED LINKS</span></span>
