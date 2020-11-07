---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943685"
---
# <span data-ttu-id="13a3d-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="13a3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="13a3d-103">Obtém um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="13a3d-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="13a3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13a3d-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13a3d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="13a3d-106">O cmdlet **Get-AzCdnProfile** Obtém um perfil da CDN (rede de distribuição de conteúdo) do Azure e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="13a3d-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="13a3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13a3d-107">EXAMPLES</span></span>

## <span data-ttu-id="13a3d-108">OS</span><span class="sxs-lookup"><span data-stu-id="13a3d-108">PARAMETERS</span></span>

### <span data-ttu-id="13a3d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-109">-DefaultProfile</span></span>
<span data-ttu-id="13a3d-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="13a3d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13a3d-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="13a3d-111">-ProfileName</span></span>
<span data-ttu-id="13a3d-112">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="13a3d-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="13a3d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a3d-113">-ResourceGroupName</span></span>
<span data-ttu-id="13a3d-114">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="13a3d-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="13a3d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a3d-115">CommonParameters</span></span>
<span data-ttu-id="13a3d-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a3d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a3d-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13a3d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a3d-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13a3d-118">INPUTS</span></span>

### <span data-ttu-id="13a3d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="13a3d-119">System.String</span></span>

## <span data-ttu-id="13a3d-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13a3d-120">OUTPUTS</span></span>

### <span data-ttu-id="13a3d-121">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="13a3d-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13a3d-122">NOTES</span></span>

## <span data-ttu-id="13a3d-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13a3d-123">RELATED LINKS</span></span>

[<span data-ttu-id="13a3d-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="13a3d-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="13a3d-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="13a3d-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


