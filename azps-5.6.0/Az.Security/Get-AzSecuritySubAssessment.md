---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893115"
---
# <span data-ttu-id="80be2-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="80be2-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="80be2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80be2-102">SYNOPSIS</span></span>
<span data-ttu-id="80be2-103">Obtém resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="80be2-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="80be2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80be2-104">SYNTAX</span></span>

### <span data-ttu-id="80be2-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80be2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80be2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="80be2-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80be2-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="80be2-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80be2-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="80be2-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80be2-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80be2-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80be2-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80be2-110">DESCRIPTION</span></span>
<span data-ttu-id="80be2-111">Obtém resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="80be2-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="80be2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80be2-112">EXAMPLES</span></span>

### <span data-ttu-id="80be2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80be2-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="80be2-114">Obtém todos os resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="80be2-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="80be2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80be2-115">PARAMETERS</span></span>

### <span data-ttu-id="80be2-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="80be2-116">-AssessedResourceId</span></span>
<span data-ttu-id="80be2-117">ID completa do recurso em que a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="80be2-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80be2-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="80be2-118">-AssessmentName</span></span>
<span data-ttu-id="80be2-119">Nome do recurso de avaliação.</span><span class="sxs-lookup"><span data-stu-id="80be2-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80be2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80be2-120">-DefaultProfile</span></span>
<span data-ttu-id="80be2-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80be2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80be2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="80be2-122">-Name</span></span>
<span data-ttu-id="80be2-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="80be2-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80be2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80be2-124">-ResourceId</span></span>
<span data-ttu-id="80be2-125">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="80be2-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80be2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80be2-126">CommonParameters</span></span>
<span data-ttu-id="80be2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80be2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80be2-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80be2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80be2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80be2-129">INPUTS</span></span>

### <span data-ttu-id="80be2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="80be2-130">System.String</span></span>

## <span data-ttu-id="80be2-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80be2-131">OUTPUTS</span></span>

### <span data-ttu-id="80be2-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="80be2-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="80be2-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="80be2-133">NOTES</span></span>

## <span data-ttu-id="80be2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80be2-134">RELATED LINKS</span></span>
