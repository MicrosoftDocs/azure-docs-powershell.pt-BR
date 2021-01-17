---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433267"
---
# <span data-ttu-id="a0557-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a0557-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="a0557-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0557-102">SYNOPSIS</span></span>
<span data-ttu-id="a0557-103">Obtém subavaliações resulta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0557-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a0557-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0557-104">SYNTAX</span></span>

### <span data-ttu-id="a0557-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0557-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0557-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a0557-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0557-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="a0557-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0557-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a0557-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0557-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="a0557-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0557-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0557-110">DESCRIPTION</span></span>
<span data-ttu-id="a0557-111">Obtém subavaliações resulta em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0557-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a0557-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0557-112">EXAMPLES</span></span>

### <span data-ttu-id="a0557-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0557-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="a0557-114">Obtém todas as subavaliações resultando em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0557-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="a0557-115">OS</span><span class="sxs-lookup"><span data-stu-id="a0557-115">PARAMETERS</span></span>

### <span data-ttu-id="a0557-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a0557-116">-AssessedResourceId</span></span>
<span data-ttu-id="a0557-117">ID do recurso completo do recurso no qual a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="a0557-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="a0557-118">-Assessmentname</span><span class="sxs-lookup"><span data-stu-id="a0557-118">-AssessmentName</span></span>
<span data-ttu-id="a0557-119">Nome do recurso de avaliação.</span><span class="sxs-lookup"><span data-stu-id="a0557-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="a0557-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0557-120">-DefaultProfile</span></span>
<span data-ttu-id="a0557-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0557-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0557-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0557-122">-Name</span></span>
<span data-ttu-id="a0557-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0557-123">Resource name.</span></span>

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

### <span data-ttu-id="a0557-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0557-124">-ResourceId</span></span>
<span data-ttu-id="a0557-125">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="a0557-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a0557-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0557-126">CommonParameters</span></span>
<span data-ttu-id="a0557-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0557-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0557-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0557-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0557-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0557-129">INPUTS</span></span>

### <span data-ttu-id="a0557-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0557-130">System.String</span></span>

## <span data-ttu-id="a0557-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0557-131">OUTPUTS</span></span>

### <span data-ttu-id="a0557-132">Microsoft. Azure. Commands. Security. Models. subassessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="a0557-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="a0557-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0557-133">NOTES</span></span>

## <span data-ttu-id="a0557-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0557-134">RELATED LINKS</span></span>
