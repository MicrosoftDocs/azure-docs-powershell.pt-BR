---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440444"
---
# <span data-ttu-id="cd1ae-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="cd1ae-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="cd1ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1ae-103">Cria uma marca de IP.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd1ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd1ae-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cd1ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="cd1ae-106">O cmdlet **New-AzureRmPublicIpTag** cria uma marca de IP.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="cd1ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="cd1ae-108">1: criar uma nova marca de IP</span><span class="sxs-lookup"><span data-stu-id="cd1ae-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="cd1ae-109">Esse comando cria uma nova marca de IP com o TagType como "FirstPartyUsage" e marca como "/SQL".</span><span class="sxs-lookup"><span data-stu-id="cd1ae-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="cd1ae-110">Isso é usado na criação do publicIpAddress com essas marcas específicas para alocação.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="cd1ae-111">OS</span><span class="sxs-lookup"><span data-stu-id="cd1ae-111">PARAMETERS</span></span>

### <span data-ttu-id="cd1ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1ae-112">-DefaultProfile</span></span>
<span data-ttu-id="cd1ae-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ae-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="cd1ae-114">-IpTagType</span></span>
<span data-ttu-id="cd1ae-115">IpTag digite o exemplo: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="cd1ae-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ae-116">-Marca</span><span class="sxs-lookup"><span data-stu-id="cd1ae-116">-Tag</span></span>
<span data-ttu-id="cd1ae-117">Valor IpTag exemplo:/SQL</span><span class="sxs-lookup"><span data-stu-id="cd1ae-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ae-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd1ae-118">-Confirm</span></span>
<span data-ttu-id="cd1ae-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ae-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1ae-120">-WhatIf</span></span>
<span data-ttu-id="cd1ae-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1ae-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cd1ae-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd1ae-123">INPUTS</span></span>

### <span data-ttu-id="cd1ae-124">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1ae-124">System.String</span></span>


## <span data-ttu-id="cd1ae-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd1ae-125">OUTPUTS</span></span>

### <span data-ttu-id="cd1ae-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="cd1ae-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="cd1ae-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd1ae-127">NOTES</span></span>

## <span data-ttu-id="cd1ae-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd1ae-128">RELATED LINKS</span></span>

