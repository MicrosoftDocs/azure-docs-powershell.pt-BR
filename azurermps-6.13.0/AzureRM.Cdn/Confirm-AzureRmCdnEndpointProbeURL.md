---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/confirm-azurermcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Confirm-AzureRmCdnEndpointProbeURL.md
ms.openlocfilehash: d6cf25c352c89592112aaa0a60cf7ba14ff7acf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431397"
---
# <span data-ttu-id="40873-101">Confirm-AzureRmCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="40873-101">Confirm-AzureRmCdnEndpointProbeURL</span></span>

## <span data-ttu-id="40873-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40873-102">SYNOPSIS</span></span>
<span data-ttu-id="40873-103">Valida uma URL de teste.</span><span class="sxs-lookup"><span data-stu-id="40873-103">Validates a probe URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40873-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40873-104">SYNTAX</span></span>

```
Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40873-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40873-105">DESCRIPTION</span></span>
<span data-ttu-id="40873-106">O cmdlet **Confirm-AzureRmCdnEndpointProbeURL** confirma se a URL do teste fornecida pode ser usada para a aceleração dinâmica do site.</span><span class="sxs-lookup"><span data-stu-id="40873-106">The **Confirm-AzureRmCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="40873-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40873-107">EXAMPLES</span></span>

### <span data-ttu-id="40873-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40873-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzureRmCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="40873-109">Valida a URL de teste " http://www.bing.com/images "</span><span class="sxs-lookup"><span data-stu-id="40873-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="40873-110">OS</span><span class="sxs-lookup"><span data-stu-id="40873-110">PARAMETERS</span></span>

### <span data-ttu-id="40873-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40873-111">-DefaultProfile</span></span>
<span data-ttu-id="40873-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40873-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40873-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="40873-113">-ProbeUrl</span></span>
<span data-ttu-id="40873-114">Nome da URL do teste proposto a ser validado.</span><span class="sxs-lookup"><span data-stu-id="40873-114">Proposed probe URL name to validate.</span></span>

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

### <span data-ttu-id="40873-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40873-115">CommonParameters</span></span>
<span data-ttu-id="40873-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40873-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40873-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40873-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40873-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40873-118">INPUTS</span></span>

### <span data-ttu-id="40873-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40873-119">None</span></span>

## <span data-ttu-id="40873-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40873-120">OUTPUTS</span></span>

### <span data-ttu-id="40873-121">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="40873-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="40873-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40873-122">NOTES</span></span>

## <span data-ttu-id="40873-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40873-123">RELATED LINKS</span></span>
