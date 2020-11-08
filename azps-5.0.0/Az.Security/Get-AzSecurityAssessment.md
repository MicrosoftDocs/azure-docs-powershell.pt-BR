---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125406"
---
# <span data-ttu-id="f8c1e-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="f8c1e-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="f8c1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c1e-103">Obtém avaliações de segurança e seus resultados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="f8c1e-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="f8c1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8c1e-104">SYNTAX</span></span>

### <span data-ttu-id="f8c1e-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="f8c1e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c1e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f8c1e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c1e-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="f8c1e-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8c1e-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="f8c1e-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8c1e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f8c1e-109">DESCRIPTION</span></span>
<span data-ttu-id="f8c1e-110">Obtém a avaliação de segurança e seus resultados na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="f8c1e-111">As avaliações de segurança permitirão que você saiba quais práticas recomendadas são refeitas pela central de segurança do Azure para serem reduzidas na sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="f8c1e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f8c1e-112">EXAMPLES</span></span>

### <span data-ttu-id="f8c1e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8c1e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="f8c1e-114">Obtém toda a avaliação de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="f8c1e-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="f8c1e-115">OS</span><span class="sxs-lookup"><span data-stu-id="f8c1e-115">PARAMETERS</span></span>

### <span data-ttu-id="f8c1e-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c1e-116">-AssessedResourceId</span></span>
<span data-ttu-id="f8c1e-117">ID do recurso completo do recurso no qual a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="f8c1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c1e-118">-DefaultProfile</span></span>
<span data-ttu-id="f8c1e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c1e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8c1e-120">-Name</span></span>
<span data-ttu-id="f8c1e-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-121">Resource name.</span></span>

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

### <span data-ttu-id="f8c1e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c1e-122">-ResourceId</span></span>
<span data-ttu-id="f8c1e-123">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f8c1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c1e-124">CommonParameters</span></span>
<span data-ttu-id="f8c1e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c1e-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8c1e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c1e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f8c1e-127">INPUTS</span></span>

### <span data-ttu-id="f8c1e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c1e-128">System.String</span></span>

## <span data-ttu-id="f8c1e-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f8c1e-129">OUTPUTS</span></span>

### <span data-ttu-id="f8c1e-130">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="f8c1e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="f8c1e-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f8c1e-131">NOTES</span></span>

## <span data-ttu-id="f8c1e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8c1e-132">RELATED LINKS</span></span>
