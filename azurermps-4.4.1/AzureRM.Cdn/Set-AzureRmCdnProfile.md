---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 8e294b457d93c5e9aeb9f8391fccdedc3ccfd778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431130"
---
# <span data-ttu-id="55739-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="55739-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="55739-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55739-102">SYNOPSIS</span></span>
<span data-ttu-id="55739-103">Atualiza um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="55739-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55739-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55739-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55739-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55739-105">DESCRIPTION</span></span>
<span data-ttu-id="55739-106">O cmdlet **set-AzureRmCdnProfile** atualiza um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="55739-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="55739-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55739-107">EXAMPLES</span></span>

## <span data-ttu-id="55739-108">OS</span><span class="sxs-lookup"><span data-stu-id="55739-108">PARAMETERS</span></span>

### <span data-ttu-id="55739-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="55739-109">-CdnProfile</span></span>
<span data-ttu-id="55739-110">Especifica o perfil que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="55739-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="55739-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55739-111">-Confirm</span></span>
<span data-ttu-id="55739-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55739-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55739-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55739-113">-WhatIf</span></span>
<span data-ttu-id="55739-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55739-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55739-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55739-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55739-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55739-116">-DefaultProfile</span></span>
<span data-ttu-id="55739-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55739-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55739-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55739-118">CommonParameters</span></span>
<span data-ttu-id="55739-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55739-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55739-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55739-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55739-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55739-121">INPUTS</span></span>

### <span data-ttu-id="55739-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="55739-122">PSProfile</span></span>
<span data-ttu-id="55739-123">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="55739-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="55739-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55739-124">OUTPUTS</span></span>

### <span data-ttu-id="55739-125">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="55739-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="55739-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55739-126">NOTES</span></span>

## <span data-ttu-id="55739-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55739-127">RELATED LINKS</span></span>

[<span data-ttu-id="55739-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="55739-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="55739-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="55739-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="55739-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="55739-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


