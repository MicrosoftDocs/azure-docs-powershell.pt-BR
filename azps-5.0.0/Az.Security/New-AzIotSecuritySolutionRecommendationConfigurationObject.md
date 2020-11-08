---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116194"
---
# <span data-ttu-id="24d0d-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="24d0d-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="24d0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="24d0d-103">Criar uma nova configuração de recomendação para a solução de segurança IOT</span><span class="sxs-lookup"><span data-stu-id="24d0d-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="24d0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24d0d-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24d0d-105">DESCRIPTION</span></span>
<span data-ttu-id="24d0d-106">O AzIotSecuritySolutionRecommendationConfigurationObject cria um novo objeto de configuração de recomendação para a solução de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="24d0d-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="24d0d-107">Dessa forma, o status de uma recomendação é configurado, seja habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="24d0d-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="24d0d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24d0d-108">EXAMPLES</span></span>

### <span data-ttu-id="24d0d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24d0d-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="24d0d-110">Criar uma nova configuração de recomendação para o tipo de recomendação "IoT_ACRAuthentication" com o status definido como Disable</span><span class="sxs-lookup"><span data-stu-id="24d0d-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="24d0d-111">OS</span><span class="sxs-lookup"><span data-stu-id="24d0d-111">PARAMETERS</span></span>

### <span data-ttu-id="24d0d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d0d-112">-DefaultProfile</span></span>
<span data-ttu-id="24d0d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24d0d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d0d-114">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="24d0d-114">-Enabled</span></span>
<span data-ttu-id="24d0d-115">Situação.</span><span class="sxs-lookup"><span data-stu-id="24d0d-115">Status .</span></span>

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

### <span data-ttu-id="24d0d-116">-Recomendaçãotype</span><span class="sxs-lookup"><span data-stu-id="24d0d-116">-RecommendationType</span></span>
<span data-ttu-id="24d0d-117">Tipo de recomendação.</span><span class="sxs-lookup"><span data-stu-id="24d0d-117">Recommendation type.</span></span>

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

### <span data-ttu-id="24d0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d0d-118">CommonParameters</span></span>
<span data-ttu-id="24d0d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d0d-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24d0d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d0d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24d0d-121">INPUTS</span></span>

### <span data-ttu-id="24d0d-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="24d0d-122">None</span></span>

## <span data-ttu-id="24d0d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24d0d-123">OUTPUTS</span></span>

### <span data-ttu-id="24d0d-124">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="24d0d-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="24d0d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24d0d-125">NOTES</span></span>

## <span data-ttu-id="24d0d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24d0d-126">RELATED LINKS</span></span>
