---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111183"
---
# <span data-ttu-id="eb295-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="eb295-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb295-102">SYNOPSIS</span></span>
<span data-ttu-id="eb295-103">Atualiza um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="eb295-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="eb295-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb295-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb295-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb295-105">DESCRIPTION</span></span>
<span data-ttu-id="eb295-106">O cmdlet **Set-AzCdnProfile** atualiza um perfil de REDE de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb295-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="eb295-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb295-107">EXAMPLES</span></span>

## <span data-ttu-id="eb295-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb295-108">PARAMETERS</span></span>

### <span data-ttu-id="eb295-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-109">-CdnProfile</span></span>
<span data-ttu-id="eb295-110">Especifica o perfil que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="eb295-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="eb295-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-111">-DefaultProfile</span></span>
<span data-ttu-id="eb295-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="eb295-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb295-113">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eb295-113">-Confirm</span></span>
<span data-ttu-id="eb295-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb295-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb295-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb295-115">-WhatIf</span></span>
<span data-ttu-id="eb295-116">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eb295-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb295-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb295-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb295-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb295-118">CommonParameters</span></span>
<span data-ttu-id="eb295-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb295-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb295-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb295-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb295-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="eb295-121">INPUTS</span></span>

### <span data-ttu-id="eb295-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="eb295-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="eb295-123">OUTPUTS</span></span>

### <span data-ttu-id="eb295-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="eb295-125">Notas</span><span class="sxs-lookup"><span data-stu-id="eb295-125">NOTES</span></span>

## <span data-ttu-id="eb295-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb295-126">RELATED LINKS</span></span>

[<span data-ttu-id="eb295-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="eb295-128">Novo-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="eb295-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eb295-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


