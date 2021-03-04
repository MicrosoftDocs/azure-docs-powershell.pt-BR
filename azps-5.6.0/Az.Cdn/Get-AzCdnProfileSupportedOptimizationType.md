---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890020"
---
# <span data-ttu-id="b3454-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="b3454-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="b3454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3454-102">SYNOPSIS</span></span>
<span data-ttu-id="b3454-103">Obtém os tipos de otimização com suporte para um perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="b3454-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="b3454-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b3454-104">SYNTAX</span></span>

### <span data-ttu-id="b3454-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3454-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3454-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3454-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3454-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b3454-107">DESCRIPTION</span></span>
<span data-ttu-id="b3454-108">O cmdlet **Get-AzCdnProfileSupportedOptimizationType** obtém os tipos de otimização com suporte para o perfil atual.</span><span class="sxs-lookup"><span data-stu-id="b3454-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="b3454-109">Um usuário pode criar um ponto de extremidade com um tipo de otimização a partir dos valores listados.</span><span class="sxs-lookup"><span data-stu-id="b3454-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="b3454-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3454-110">EXAMPLES</span></span>

### <span data-ttu-id="b3454-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3454-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="b3454-112">Obter os tipos de otimização com suporte para um perfil cdn.</span><span class="sxs-lookup"><span data-stu-id="b3454-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="b3454-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b3454-113">PARAMETERS</span></span>

### <span data-ttu-id="b3454-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b3454-114">-CdnProfile</span></span>
<span data-ttu-id="b3454-115">O objeto de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3454-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="b3454-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3454-116">-DefaultProfile</span></span>
<span data-ttu-id="b3454-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3454-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3454-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b3454-118">-ProfileName</span></span>
<span data-ttu-id="b3454-119">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="b3454-119">The name of the profile.</span></span>

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

### <span data-ttu-id="b3454-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3454-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3454-121">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="b3454-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="b3454-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3454-122">CommonParameters</span></span>
<span data-ttu-id="b3454-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3454-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3454-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3454-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3454-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3454-125">INPUTS</span></span>

### <span data-ttu-id="b3454-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="b3454-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b3454-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b3454-127">OUTPUTS</span></span>

### <span data-ttu-id="b3454-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="b3454-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="b3454-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="b3454-129">NOTES</span></span>

## <span data-ttu-id="b3454-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3454-130">RELATED LINKS</span></span>
