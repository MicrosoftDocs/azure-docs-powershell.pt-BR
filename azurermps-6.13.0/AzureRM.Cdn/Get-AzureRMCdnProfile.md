---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440096"
---
# <span data-ttu-id="69789-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69789-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="69789-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69789-102">SYNOPSIS</span></span>
<span data-ttu-id="69789-103">Obtém um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="69789-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69789-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69789-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69789-105">DESCRIPTION</span></span>
<span data-ttu-id="69789-106">O cmdlet **Get-AzureRMCdnProfile** Obtém um perfil da CDN (rede de distribuição de conteúdo) do Azure e suas informações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="69789-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="69789-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69789-107">EXAMPLES</span></span>

## <span data-ttu-id="69789-108">OS</span><span class="sxs-lookup"><span data-stu-id="69789-108">PARAMETERS</span></span>

### <span data-ttu-id="69789-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69789-109">-DefaultProfile</span></span>
<span data-ttu-id="69789-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="69789-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69789-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="69789-111">-ProfileName</span></span>
<span data-ttu-id="69789-112">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="69789-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="69789-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69789-113">-ResourceGroupName</span></span>
<span data-ttu-id="69789-114">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="69789-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="69789-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69789-115">CommonParameters</span></span>
<span data-ttu-id="69789-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69789-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69789-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69789-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69789-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69789-118">INPUTS</span></span>

### <span data-ttu-id="69789-119">System. String</span><span class="sxs-lookup"><span data-stu-id="69789-119">System.String</span></span>

## <span data-ttu-id="69789-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69789-120">OUTPUTS</span></span>

### <span data-ttu-id="69789-121">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="69789-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="69789-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69789-122">NOTES</span></span>

## <span data-ttu-id="69789-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69789-123">RELATED LINKS</span></span>

[<span data-ttu-id="69789-124">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69789-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="69789-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69789-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="69789-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="69789-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


