---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 677c67ecc2418a4940b4cbe79e2ac7145eada0c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889405"
---
# <span data-ttu-id="b7191-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b7191-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="b7191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7191-102">SYNOPSIS</span></span>
<span data-ttu-id="b7191-103">Criar nova configuração de recomendação para solução de segurança de iot</span><span class="sxs-lookup"><span data-stu-id="b7191-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="b7191-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7191-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7191-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7191-105">DESCRIPTION</span></span>
<span data-ttu-id="b7191-106">O AzIotSecuritySolutionRecommendationConfigurationObject cria um novo objeto de configuração de recomendação para solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="b7191-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="b7191-107">Dessa forma, o status de uma recomendação é configurado, seja ele habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b7191-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="b7191-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7191-108">EXAMPLES</span></span>

### <span data-ttu-id="b7191-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7191-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="b7191-110">Criar nova configuração de recomendação para o tipo de recomendação "IoT_ACRAuthentication" com status definido para desabilitar</span><span class="sxs-lookup"><span data-stu-id="b7191-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="b7191-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7191-111">PARAMETERS</span></span>

### <span data-ttu-id="b7191-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7191-112">-DefaultProfile</span></span>
<span data-ttu-id="b7191-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7191-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7191-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b7191-114">-Enabled</span></span>
<span data-ttu-id="b7191-115">Status .</span><span class="sxs-lookup"><span data-stu-id="b7191-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7191-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="b7191-116">-RecommendationType</span></span>
<span data-ttu-id="b7191-117">Tipo de recomendação.</span><span class="sxs-lookup"><span data-stu-id="b7191-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7191-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7191-118">CommonParameters</span></span>
<span data-ttu-id="b7191-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7191-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7191-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7191-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7191-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7191-121">INPUTS</span></span>

### <span data-ttu-id="b7191-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7191-122">None</span></span>

## <span data-ttu-id="b7191-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7191-123">OUTPUTS</span></span>

### <span data-ttu-id="b7191-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7191-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="b7191-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7191-125">NOTES</span></span>

## <span data-ttu-id="b7191-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7191-126">RELATED LINKS</span></span>
