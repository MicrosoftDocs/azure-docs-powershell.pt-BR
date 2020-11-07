---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942831"
---
# <span data-ttu-id="58d04-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="58d04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58d04-102">SYNOPSIS</span></span>
<span data-ttu-id="58d04-103">Atualiza um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="58d04-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="58d04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d04-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58d04-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58d04-105">DESCRIPTION</span></span>
<span data-ttu-id="58d04-106">O cmdlet **set-AzCdnEndpoint** atualiza um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="58d04-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="58d04-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58d04-107">EXAMPLES</span></span>

## <span data-ttu-id="58d04-108">OS</span><span class="sxs-lookup"><span data-stu-id="58d04-108">PARAMETERS</span></span>

### <span data-ttu-id="58d04-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-109">-CdnEndpoint</span></span>
<span data-ttu-id="58d04-110">Especifica o ponto de extremidade que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="58d04-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="58d04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d04-111">-DefaultProfile</span></span>
<span data-ttu-id="58d04-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58d04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58d04-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58d04-113">-Confirm</span></span>
<span data-ttu-id="58d04-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58d04-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d04-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d04-115">-WhatIf</span></span>
<span data-ttu-id="58d04-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58d04-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d04-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58d04-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d04-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d04-118">CommonParameters</span></span>
<span data-ttu-id="58d04-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d04-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d04-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58d04-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d04-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58d04-121">INPUTS</span></span>

### <span data-ttu-id="58d04-122">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="58d04-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58d04-123">OUTPUTS</span></span>

### <span data-ttu-id="58d04-124">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="58d04-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58d04-125">NOTES</span></span>

## <span data-ttu-id="58d04-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58d04-126">RELATED LINKS</span></span>

[<span data-ttu-id="58d04-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="58d04-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="58d04-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="58d04-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="58d04-131">Parar-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d04-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


