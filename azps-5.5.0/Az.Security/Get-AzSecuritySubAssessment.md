---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112614"
---
# <span data-ttu-id="ace6b-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="ace6b-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="ace6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ace6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ace6b-103">Obtém resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ace6b-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="ace6b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ace6b-104">SYNTAX</span></span>

### <span data-ttu-id="ace6b-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ace6b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ace6b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ace6b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace6b-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="ace6b-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace6b-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="ace6b-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ace6b-109">Resourceid</span><span class="sxs-lookup"><span data-stu-id="ace6b-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ace6b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ace6b-110">DESCRIPTION</span></span>
<span data-ttu-id="ace6b-111">Obtém resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ace6b-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="ace6b-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ace6b-112">EXAMPLES</span></span>

### <span data-ttu-id="ace6b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ace6b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="ace6b-114">Obtém todos os resultados de subavaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="ace6b-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="ace6b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ace6b-115">PARAMETERS</span></span>

### <span data-ttu-id="ace6b-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="ace6b-116">-AssessedResourceId</span></span>
<span data-ttu-id="ace6b-117">ID completa do recurso em que a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="ace6b-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="ace6b-118">-NomedaAvaliação</span><span class="sxs-lookup"><span data-stu-id="ace6b-118">-AssessmentName</span></span>
<span data-ttu-id="ace6b-119">Nome do recurso de avaliação.</span><span class="sxs-lookup"><span data-stu-id="ace6b-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="ace6b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace6b-120">-DefaultProfile</span></span>
<span data-ttu-id="ace6b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ace6b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace6b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ace6b-122">-Name</span></span>
<span data-ttu-id="ace6b-123">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ace6b-123">Resource name.</span></span>

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

### <span data-ttu-id="ace6b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace6b-124">-ResourceId</span></span>
<span data-ttu-id="ace6b-125">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="ace6b-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ace6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace6b-126">CommonParameters</span></span>
<span data-ttu-id="ace6b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace6b-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ace6b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace6b-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="ace6b-129">INPUTS</span></span>

### <span data-ttu-id="ace6b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ace6b-130">System.String</span></span>

## <span data-ttu-id="ace6b-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="ace6b-131">OUTPUTS</span></span>

### <span data-ttu-id="ace6b-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="ace6b-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="ace6b-133">Notas</span><span class="sxs-lookup"><span data-stu-id="ace6b-133">NOTES</span></span>

## <span data-ttu-id="ace6b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ace6b-134">RELATED LINKS</span></span>
