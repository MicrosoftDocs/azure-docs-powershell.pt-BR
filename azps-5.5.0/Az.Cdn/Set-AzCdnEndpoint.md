---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117909"
---
# <span data-ttu-id="4735a-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="4735a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4735a-102">SYNOPSIS</span></span>
<span data-ttu-id="4735a-103">Atualiza um ponto de extremidade de CDN.</span><span class="sxs-lookup"><span data-stu-id="4735a-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="4735a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4735a-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4735a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4735a-105">DESCRIPTION</span></span>
<span data-ttu-id="4735a-106">O cmdlet **Set-AzCdnEndpoint** atualiza um ponto de extremidade de REDE de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="4735a-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4735a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4735a-107">EXAMPLES</span></span>

## <span data-ttu-id="4735a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4735a-108">PARAMETERS</span></span>

### <span data-ttu-id="4735a-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-109">-CdnEndpoint</span></span>
<span data-ttu-id="4735a-110">Especifica o ponto de extremidade que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="4735a-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="4735a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4735a-111">-DefaultProfile</span></span>
<span data-ttu-id="4735a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4735a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4735a-113">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4735a-113">-Confirm</span></span>
<span data-ttu-id="4735a-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4735a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4735a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4735a-115">-WhatIf</span></span>
<span data-ttu-id="4735a-116">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4735a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4735a-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4735a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4735a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4735a-118">CommonParameters</span></span>
<span data-ttu-id="4735a-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4735a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4735a-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4735a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4735a-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="4735a-121">INPUTS</span></span>

### <span data-ttu-id="4735a-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4735a-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="4735a-123">OUTPUTS</span></span>

### <span data-ttu-id="4735a-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4735a-125">Notas</span><span class="sxs-lookup"><span data-stu-id="4735a-125">NOTES</span></span>

## <span data-ttu-id="4735a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4735a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4735a-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="4735a-128">Novo-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="4735a-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="4735a-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="4735a-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4735a-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


