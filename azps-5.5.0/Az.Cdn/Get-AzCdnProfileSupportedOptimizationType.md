---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115511"
---
# <span data-ttu-id="0717b-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="0717b-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="0717b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0717b-102">SYNOPSIS</span></span>
<span data-ttu-id="0717b-103">Obtém os tipos de otimização com suporte para um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="0717b-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="0717b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0717b-104">SYNTAX</span></span>

### <span data-ttu-id="0717b-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0717b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0717b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0717b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0717b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0717b-107">DESCRIPTION</span></span>
<span data-ttu-id="0717b-108">O cmdlet **Get-AzCdnProfileSupportedOptimizationType obtém** os tipos de otimização com suporte para o perfil atual.</span><span class="sxs-lookup"><span data-stu-id="0717b-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="0717b-109">Um usuário pode criar um ponto de extremidade com um tipo de otimização a partir dos valores listados.</span><span class="sxs-lookup"><span data-stu-id="0717b-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="0717b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0717b-110">EXAMPLES</span></span>

### <span data-ttu-id="0717b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0717b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="0717b-112">Obter os tipos de otimização com suporte para um perfil de CDN.</span><span class="sxs-lookup"><span data-stu-id="0717b-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="0717b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0717b-113">PARAMETERS</span></span>

### <span data-ttu-id="0717b-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0717b-114">-CdnProfile</span></span>
<span data-ttu-id="0717b-115">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="0717b-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="0717b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0717b-116">-DefaultProfile</span></span>
<span data-ttu-id="0717b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0717b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0717b-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0717b-118">-ProfileName</span></span>
<span data-ttu-id="0717b-119">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="0717b-119">The name of the profile.</span></span>

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

### <span data-ttu-id="0717b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0717b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0717b-121">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="0717b-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0717b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0717b-122">CommonParameters</span></span>
<span data-ttu-id="0717b-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0717b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0717b-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0717b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0717b-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="0717b-125">INPUTS</span></span>

### <span data-ttu-id="0717b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="0717b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="0717b-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="0717b-127">OUTPUTS</span></span>

### <span data-ttu-id="0717b-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="0717b-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="0717b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="0717b-129">NOTES</span></span>

## <span data-ttu-id="0717b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0717b-130">RELATED LINKS</span></span>
