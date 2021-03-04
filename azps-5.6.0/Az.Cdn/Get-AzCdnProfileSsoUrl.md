---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886798"
---
# <span data-ttu-id="30c6e-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="30c6e-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="30c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="30c6e-103">Obtém a URL de entrada única de um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="30c6e-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="30c6e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="30c6e-104">SYNTAX</span></span>

### <span data-ttu-id="30c6e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30c6e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30c6e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30c6e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c6e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="30c6e-107">DESCRIPTION</span></span>
<span data-ttu-id="30c6e-108">O cmdlet **Get-AzCdnProfileSsoUrl** obtém a URL de entrada única do perfil CDN (Rede de Entrega de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="30c6e-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="30c6e-109">Essa URL permite que os usuários se conectem a um portal complementar e usem recursos adicionais da CDN.</span><span class="sxs-lookup"><span data-stu-id="30c6e-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="30c6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30c6e-110">EXAMPLES</span></span>

## <span data-ttu-id="30c6e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="30c6e-111">PARAMETERS</span></span>

### <span data-ttu-id="30c6e-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="30c6e-112">-CdnProfile</span></span>
<span data-ttu-id="30c6e-113">Especifica o perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="30c6e-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c6e-114">-DefaultProfile</span></span>
<span data-ttu-id="30c6e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="30c6e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30c6e-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="30c6e-116">-ProfileName</span></span>
<span data-ttu-id="30c6e-117">Especifica o nome do perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="30c6e-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="30c6e-119">Especifica o nome do nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="30c6e-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c6e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c6e-120">CommonParameters</span></span>
<span data-ttu-id="30c6e-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c6e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c6e-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30c6e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c6e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30c6e-123">INPUTS</span></span>

### <span data-ttu-id="30c6e-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="30c6e-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="30c6e-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="30c6e-125">OUTPUTS</span></span>

### <span data-ttu-id="30c6e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="30c6e-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="30c6e-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="30c6e-127">NOTES</span></span>

## <span data-ttu-id="30c6e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30c6e-128">RELATED LINKS</span></span>

[<span data-ttu-id="30c6e-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="30c6e-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


