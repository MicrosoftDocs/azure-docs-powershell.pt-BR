---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 5a8a09955158c21ff6d52e2327370c48448c12d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892720"
---
# <span data-ttu-id="a07d1-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a07d1-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="a07d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a07d1-103">Obtém avaliações de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a07d1-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="a07d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a07d1-104">SYNTAX</span></span>

### <span data-ttu-id="a07d1-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a07d1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07d1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a07d1-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07d1-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a07d1-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a07d1-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a07d1-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a07d1-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a07d1-109">DESCRIPTION</span></span>
<span data-ttu-id="a07d1-110">Obtém avaliação de segurança e seus resultados na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a07d1-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="a07d1-111">As avaliações de segurança permitirão que você saiba quais práticas recomendadas são recomendadas pelo Centro de Segurança do Azure para serem atenuadas em sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d1-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="a07d1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a07d1-112">EXAMPLES</span></span>

### <span data-ttu-id="a07d1-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a07d1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="a07d1-114">Obtém toda a avaliação de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a07d1-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="a07d1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a07d1-115">PARAMETERS</span></span>

### <span data-ttu-id="a07d1-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a07d1-116">-AssessedResourceId</span></span>
<span data-ttu-id="a07d1-117">ID completa do recurso em que a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="a07d1-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07d1-118">-DefaultProfile</span></span>
<span data-ttu-id="a07d1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07d1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a07d1-120">-Name</span></span>
<span data-ttu-id="a07d1-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a07d1-121">Resource name.</span></span>

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
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a07d1-122">-ResourceId</span></span>
<span data-ttu-id="a07d1-123">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="a07d1-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a07d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07d1-124">CommonParameters</span></span>
<span data-ttu-id="a07d1-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07d1-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a07d1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07d1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a07d1-127">INPUTS</span></span>

### <span data-ttu-id="a07d1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a07d1-128">System.String</span></span>

## <span data-ttu-id="a07d1-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a07d1-129">OUTPUTS</span></span>

### <span data-ttu-id="a07d1-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a07d1-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a07d1-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a07d1-131">NOTES</span></span>

## <span data-ttu-id="a07d1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a07d1-132">RELATED LINKS</span></span>
