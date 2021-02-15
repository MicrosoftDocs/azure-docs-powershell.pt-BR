---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112188"
---
# <span data-ttu-id="37ba9-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="37ba9-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="37ba9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="37ba9-103">Valida uma URL de negociação.</span><span class="sxs-lookup"><span data-stu-id="37ba9-103">Validates a probe URL.</span></span>

## <span data-ttu-id="37ba9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37ba9-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37ba9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="37ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="37ba9-106">O cmdlet **Confirm-AzCdnEndpointProbeURL** confirma se a URL fornecida pode ser usada para aceleração dinâmica do site.</span><span class="sxs-lookup"><span data-stu-id="37ba9-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="37ba9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37ba9-107">EXAMPLES</span></span>

### <span data-ttu-id="37ba9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37ba9-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="37ba9-109">Valida a url da url " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="37ba9-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="37ba9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37ba9-110">PARAMETERS</span></span>

### <span data-ttu-id="37ba9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ba9-111">-DefaultProfile</span></span>
<span data-ttu-id="37ba9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37ba9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ba9-113">-Eleurl</span><span class="sxs-lookup"><span data-stu-id="37ba9-113">-ProbeUrl</span></span>
<span data-ttu-id="37ba9-114">Nome de URL proposto para validação.</span><span class="sxs-lookup"><span data-stu-id="37ba9-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="37ba9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ba9-115">CommonParameters</span></span>
<span data-ttu-id="37ba9-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ba9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ba9-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37ba9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ba9-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="37ba9-118">INPUTS</span></span>

### <span data-ttu-id="37ba9-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37ba9-119">None</span></span>

## <span data-ttu-id="37ba9-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="37ba9-120">OUTPUTS</span></span>

### <span data-ttu-id="37ba9-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="37ba9-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="37ba9-122">Notas</span><span class="sxs-lookup"><span data-stu-id="37ba9-122">NOTES</span></span>

## <span data-ttu-id="37ba9-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37ba9-123">RELATED LINKS</span></span>
