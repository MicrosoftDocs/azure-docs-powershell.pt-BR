---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117165"
---
# <span data-ttu-id="45ef1-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="45ef1-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="45ef1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="45ef1-103">Criar nova configuração de recomendação para solução de segurança iot</span><span class="sxs-lookup"><span data-stu-id="45ef1-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="45ef1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45ef1-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45ef1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="45ef1-106">O AzIotSecuritySolutionRecommendationConfigurationObject cria um novo objeto de configuração de recomendação para uma solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="45ef1-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="45ef1-107">Dessa forma, o status de uma recomendação é configurado, seja ele habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="45ef1-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="45ef1-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45ef1-108">EXAMPLES</span></span>

### <span data-ttu-id="45ef1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45ef1-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="45ef1-110">Criar nova configuração de recomendação para o tipo de recomendação "IoT_ACRAuthentication" com status definido para desabilitar</span><span class="sxs-lookup"><span data-stu-id="45ef1-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="45ef1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45ef1-111">PARAMETERS</span></span>

### <span data-ttu-id="45ef1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ef1-112">-DefaultProfile</span></span>
<span data-ttu-id="45ef1-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45ef1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ef1-114">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="45ef1-114">-Enabled</span></span>
<span data-ttu-id="45ef1-115">Status.</span><span class="sxs-lookup"><span data-stu-id="45ef1-115">Status .</span></span>

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

### <span data-ttu-id="45ef1-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="45ef1-116">-RecommendationType</span></span>
<span data-ttu-id="45ef1-117">Tipo de recomendação.</span><span class="sxs-lookup"><span data-stu-id="45ef1-117">Recommendation type.</span></span>

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

### <span data-ttu-id="45ef1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ef1-118">CommonParameters</span></span>
<span data-ttu-id="45ef1-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ef1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ef1-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45ef1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ef1-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="45ef1-121">INPUTS</span></span>

### <span data-ttu-id="45ef1-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="45ef1-122">None</span></span>

## <span data-ttu-id="45ef1-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="45ef1-123">OUTPUTS</span></span>

### <span data-ttu-id="45ef1-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="45ef1-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="45ef1-125">Notas</span><span class="sxs-lookup"><span data-stu-id="45ef1-125">NOTES</span></span>

## <span data-ttu-id="45ef1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45ef1-126">RELATED LINKS</span></span>
