---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942828"
---
# <span data-ttu-id="4c651-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="4c651-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c651-102">SYNOPSIS</span></span>
<span data-ttu-id="4c651-103">Atualiza um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="4c651-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="4c651-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c651-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c651-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c651-105">DESCRIPTION</span></span>
<span data-ttu-id="4c651-106">O cmdlet **set-AzCdnProfile** atualiza um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c651-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4c651-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c651-107">EXAMPLES</span></span>

## <span data-ttu-id="4c651-108">OS</span><span class="sxs-lookup"><span data-stu-id="4c651-108">PARAMETERS</span></span>

### <span data-ttu-id="4c651-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-109">-CdnProfile</span></span>
<span data-ttu-id="4c651-110">Especifica o perfil que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="4c651-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c651-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-111">-DefaultProfile</span></span>
<span data-ttu-id="4c651-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4c651-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c651-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c651-113">-Confirm</span></span>
<span data-ttu-id="4c651-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c651-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c651-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c651-115">-WhatIf</span></span>
<span data-ttu-id="4c651-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c651-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c651-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c651-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c651-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c651-118">CommonParameters</span></span>
<span data-ttu-id="4c651-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c651-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c651-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c651-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c651-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c651-121">INPUTS</span></span>

### <span data-ttu-id="4c651-122">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4c651-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c651-123">OUTPUTS</span></span>

### <span data-ttu-id="4c651-124">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4c651-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c651-125">NOTES</span></span>

## <span data-ttu-id="4c651-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c651-126">RELATED LINKS</span></span>

[<span data-ttu-id="4c651-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="4c651-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="4c651-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c651-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


