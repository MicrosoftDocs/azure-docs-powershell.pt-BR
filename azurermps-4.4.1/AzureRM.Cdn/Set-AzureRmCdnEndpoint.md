---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431134"
---
# <span data-ttu-id="f40b4-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="f40b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f40b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f40b4-103">Atualiza um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="f40b4-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f40b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f40b4-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f40b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f40b4-105">DESCRIPTION</span></span>
<span data-ttu-id="f40b4-106">O cmdlet **set-AzureRmCdnEndpoint** atualiza um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="f40b4-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f40b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f40b4-107">EXAMPLES</span></span>

## <span data-ttu-id="f40b4-108">OS</span><span class="sxs-lookup"><span data-stu-id="f40b4-108">PARAMETERS</span></span>

### <span data-ttu-id="f40b4-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-109">-CdnEndpoint</span></span>
<span data-ttu-id="f40b4-110">Especifica o ponto de extremidade que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="f40b4-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f40b4-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f40b4-111">-Confirm</span></span>
<span data-ttu-id="f40b4-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f40b4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f40b4-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f40b4-113">-WhatIf</span></span>
<span data-ttu-id="f40b4-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f40b4-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f40b4-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f40b4-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f40b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40b4-116">-DefaultProfile</span></span>
<span data-ttu-id="f40b4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f40b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f40b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40b4-118">CommonParameters</span></span>
<span data-ttu-id="f40b4-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f40b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40b4-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f40b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40b4-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f40b4-121">INPUTS</span></span>

### <span data-ttu-id="f40b4-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-122">PSEndpoint</span></span>
<span data-ttu-id="f40b4-123">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f40b4-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f40b4-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f40b4-124">OUTPUTS</span></span>

### <span data-ttu-id="f40b4-125">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f40b4-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f40b4-126">NOTES</span></span>

## <span data-ttu-id="f40b4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f40b4-127">RELATED LINKS</span></span>

[<span data-ttu-id="f40b4-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f40b4-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f40b4-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f40b4-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f40b4-132">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f40b4-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)

