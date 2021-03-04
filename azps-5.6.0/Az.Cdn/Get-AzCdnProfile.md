---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: e82e455d603ca4fd5d577e18337c93a2368fbcf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892228"
---
# <span data-ttu-id="c8bc8-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="c8bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bc8-103">Obtém um perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="c8bc8-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="c8bc8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8bc8-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8bc8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="c8bc8-106">O cmdlet **Get-AzCdnProfile** obtém um perfil cdn (Rede de Distribuição de Conteúdo) do Azure e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c8bc8-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="c8bc8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-107">EXAMPLES</span></span>

## <span data-ttu-id="c8bc8-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-108">PARAMETERS</span></span>

### <span data-ttu-id="c8bc8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-109">-DefaultProfile</span></span>
<span data-ttu-id="c8bc8-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c8bc8-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8bc8-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c8bc8-111">-ProfileName</span></span>
<span data-ttu-id="c8bc8-112">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="c8bc8-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bc8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bc8-113">-ResourceGroupName</span></span>
<span data-ttu-id="c8bc8-114">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="c8bc8-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bc8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bc8-115">CommonParameters</span></span>
<span data-ttu-id="c8bc8-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8bc8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bc8-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8bc8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bc8-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-118">INPUTS</span></span>

### <span data-ttu-id="c8bc8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="c8bc8-119">System.String</span></span>

## <span data-ttu-id="c8bc8-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-120">OUTPUTS</span></span>

### <span data-ttu-id="c8bc8-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="c8bc8-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8bc8-122">NOTES</span></span>

## <span data-ttu-id="c8bc8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8bc8-123">RELATED LINKS</span></span>

[<span data-ttu-id="c8bc8-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="c8bc8-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="c8bc8-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc8-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


