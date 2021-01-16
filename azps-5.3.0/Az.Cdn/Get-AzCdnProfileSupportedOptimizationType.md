---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430335"
---
# <span data-ttu-id="6198a-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="6198a-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="6198a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6198a-102">SYNOPSIS</span></span>
<span data-ttu-id="6198a-103">Obtém os tipos de otimização compatíveis para um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="6198a-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="6198a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6198a-104">SYNTAX</span></span>

### <span data-ttu-id="6198a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6198a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6198a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6198a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6198a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6198a-107">DESCRIPTION</span></span>
<span data-ttu-id="6198a-108">O cmdlet **Get-AzCdnProfileSupportedOptimizationType** Obtém os tipos de otimização com suporte para o perfil atual.</span><span class="sxs-lookup"><span data-stu-id="6198a-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="6198a-109">Um usuário pode criar um ponto de extremidade com um tipo de otimização dos valores listados.</span><span class="sxs-lookup"><span data-stu-id="6198a-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="6198a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6198a-110">EXAMPLES</span></span>

### <span data-ttu-id="6198a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6198a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="6198a-112">Obter os tipos de otimização compatíveis para um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="6198a-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="6198a-113">OS</span><span class="sxs-lookup"><span data-stu-id="6198a-113">PARAMETERS</span></span>

### <span data-ttu-id="6198a-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="6198a-114">-CdnProfile</span></span>
<span data-ttu-id="6198a-115">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="6198a-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="6198a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6198a-116">-DefaultProfile</span></span>
<span data-ttu-id="6198a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6198a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6198a-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6198a-118">-ProfileName</span></span>
<span data-ttu-id="6198a-119">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="6198a-119">The name of the profile.</span></span>

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

### <span data-ttu-id="6198a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6198a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6198a-121">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="6198a-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="6198a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6198a-122">CommonParameters</span></span>
<span data-ttu-id="6198a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6198a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6198a-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6198a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6198a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6198a-125">INPUTS</span></span>

### <span data-ttu-id="6198a-126">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="6198a-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="6198a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6198a-127">OUTPUTS</span></span>

### <span data-ttu-id="6198a-128">Microsoft. Azure. Commands. cdn. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="6198a-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="6198a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6198a-129">NOTES</span></span>

## <span data-ttu-id="6198a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6198a-130">RELATED LINKS</span></span>
