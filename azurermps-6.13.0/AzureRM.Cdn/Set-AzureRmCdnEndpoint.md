---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 3705cd0b20927c4b10360b7e02d507227ef2ec53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431382"
---
# <span data-ttu-id="b3b5c-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="b3b5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b5c-103">Atualiza um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3b5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3b5c-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b5c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b3b5c-106">O cmdlet **set-AzureRmCdnEndpoint** atualiza um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b3b5c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3b5c-107">EXAMPLES</span></span>

## <span data-ttu-id="b3b5c-108">OS</span><span class="sxs-lookup"><span data-stu-id="b3b5c-108">PARAMETERS</span></span>

### <span data-ttu-id="b3b5c-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-109">-CdnEndpoint</span></span>
<span data-ttu-id="b3b5c-110">Especifica o ponto de extremidade que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b5c-111">-DefaultProfile</span></span>
<span data-ttu-id="b3b5c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b3b5c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3b5c-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3b5c-113">-Confirm</span></span>
<span data-ttu-id="b3b5c-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b5c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b5c-115">-WhatIf</span></span>
<span data-ttu-id="b3b5c-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b5c-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b5c-118">CommonParameters</span></span>
<span data-ttu-id="b3b5c-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b5c-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3b5c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b5c-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3b5c-121">INPUTS</span></span>

### <span data-ttu-id="b3b5c-122">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="b3b5c-123">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3b5c-123">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="b3b5c-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3b5c-124">OUTPUTS</span></span>

### <span data-ttu-id="b3b5c-125">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b3b5c-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3b5c-126">NOTES</span></span>

## <span data-ttu-id="b3b5c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3b5c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3b5c-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b3b5c-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b3b5c-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b3b5c-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b3b5c-132">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b3b5c-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


