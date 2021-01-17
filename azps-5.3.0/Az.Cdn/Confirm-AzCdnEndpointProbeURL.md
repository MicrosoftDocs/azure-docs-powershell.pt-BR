---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434452"
---
# <span data-ttu-id="920a2-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="920a2-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="920a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="920a2-102">SYNOPSIS</span></span>
<span data-ttu-id="920a2-103">Valida uma URL de teste.</span><span class="sxs-lookup"><span data-stu-id="920a2-103">Validates a probe URL.</span></span>

## <span data-ttu-id="920a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="920a2-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="920a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="920a2-105">DESCRIPTION</span></span>
<span data-ttu-id="920a2-106">O cmdlet **Confirm-AzCdnEndpointProbeURL** confirma se a URL do teste fornecida pode ser usada para a aceleração dinâmica do site.</span><span class="sxs-lookup"><span data-stu-id="920a2-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="920a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="920a2-107">EXAMPLES</span></span>

### <span data-ttu-id="920a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="920a2-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="920a2-109">Valida a URL de teste " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="920a2-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="920a2-110">OS</span><span class="sxs-lookup"><span data-stu-id="920a2-110">PARAMETERS</span></span>

### <span data-ttu-id="920a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920a2-111">-DefaultProfile</span></span>
<span data-ttu-id="920a2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="920a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="920a2-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="920a2-113">-ProbeUrl</span></span>
<span data-ttu-id="920a2-114">Nome da URL do teste proposto a ser validado.</span><span class="sxs-lookup"><span data-stu-id="920a2-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="920a2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920a2-115">CommonParameters</span></span>
<span data-ttu-id="920a2-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="920a2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920a2-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="920a2-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920a2-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="920a2-118">INPUTS</span></span>

### <span data-ttu-id="920a2-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="920a2-119">None</span></span>

## <span data-ttu-id="920a2-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="920a2-120">OUTPUTS</span></span>

### <span data-ttu-id="920a2-121">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="920a2-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="920a2-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="920a2-122">NOTES</span></span>

## <span data-ttu-id="920a2-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="920a2-123">RELATED LINKS</span></span>
