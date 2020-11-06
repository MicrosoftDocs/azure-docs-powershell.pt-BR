---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432795"
---
# <span data-ttu-id="ef4f9-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="ef4f9-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="ef4f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4f9-103">Obtém os tipos de otimização compatíveis para um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef4f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef4f9-104">SYNTAX</span></span>

### <span data-ttu-id="ef4f9-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef4f9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef4f9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef4f9-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef4f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef4f9-107">DESCRIPTION</span></span>
<span data-ttu-id="ef4f9-108">O cmdlet **Get-AzureRmCdnProfileSupportedOptimizationType** Obtém os tipos de otimização com suporte para o perfil atual.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="ef4f9-109">Um usuário pode criar um ponto de extremidade com um tipo de otimização dos valores listados.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="ef4f9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef4f9-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4f9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef4f9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="ef4f9-112">Obter os tipos de otimização compatíveis para um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="ef4f9-113">OS</span><span class="sxs-lookup"><span data-stu-id="ef4f9-113">PARAMETERS</span></span>

### <span data-ttu-id="ef4f9-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ef4f9-114">-CdnProfile</span></span>
<span data-ttu-id="ef4f9-115">O objeto de perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="ef4f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4f9-116">-DefaultProfile</span></span>
<span data-ttu-id="ef4f9-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4f9-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ef4f9-118">-ProfileName</span></span>
<span data-ttu-id="ef4f9-119">O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-119">The name of the profile.</span></span>

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

### <span data-ttu-id="ef4f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef4f9-121">O grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ef4f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4f9-122">CommonParameters</span></span>
<span data-ttu-id="ef4f9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4f9-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4f9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4f9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef4f9-125">INPUTS</span></span>

### <span data-ttu-id="ef4f9-126">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ef4f9-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="ef4f9-127">Parâmetros: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef4f9-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="ef4f9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef4f9-128">OUTPUTS</span></span>

### <span data-ttu-id="ef4f9-129">Microsoft. Azure. Commands. cdn. Models. Profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="ef4f9-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="ef4f9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef4f9-130">NOTES</span></span>

## <span data-ttu-id="ef4f9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef4f9-131">RELATED LINKS</span></span>