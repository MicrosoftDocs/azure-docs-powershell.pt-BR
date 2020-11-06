---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 033755c47965420d3983cc8b3a4d2731ab331152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429891"
---
# <span data-ttu-id="26ae6-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="26ae6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="26ae6-103">Atualiza um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="26ae6-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26ae6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26ae6-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26ae6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="26ae6-106">O cmdlet **set-AzureRmCdnProfile** atualiza um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="26ae6-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="26ae6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26ae6-107">EXAMPLES</span></span>

## <span data-ttu-id="26ae6-108">OS</span><span class="sxs-lookup"><span data-stu-id="26ae6-108">PARAMETERS</span></span>

### <span data-ttu-id="26ae6-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-109">-CdnProfile</span></span>
<span data-ttu-id="26ae6-110">Especifica o perfil que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="26ae6-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: PSProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="26ae6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="26ae6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26ae6-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26ae6-113">-Confirm</span></span>
<span data-ttu-id="26ae6-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26ae6-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ae6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26ae6-115">-WhatIf</span></span>
<span data-ttu-id="26ae6-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26ae6-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26ae6-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26ae6-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ae6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ae6-118">CommonParameters</span></span>
<span data-ttu-id="26ae6-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ae6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ae6-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ae6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ae6-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26ae6-121">INPUTS</span></span>

### <span data-ttu-id="26ae6-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-122">PSProfile</span></span>
<span data-ttu-id="26ae6-123">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="26ae6-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="26ae6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26ae6-124">OUTPUTS</span></span>

### <span data-ttu-id="26ae6-125">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="26ae6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26ae6-126">NOTES</span></span>

## <span data-ttu-id="26ae6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26ae6-127">RELATED LINKS</span></span>

[<span data-ttu-id="26ae6-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="26ae6-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="26ae6-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="26ae6-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


