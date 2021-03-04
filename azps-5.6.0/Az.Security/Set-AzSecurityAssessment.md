---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 5bf841e055c81293d6f2f9c5811ad4e1aa1a2f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892372"
---
# <span data-ttu-id="7df43-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="7df43-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="7df43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7df43-102">SYNOPSIS</span></span>
<span data-ttu-id="7df43-103">Criar ou atualizar um resultado de avaliação de segurança em um recurso</span><span class="sxs-lookup"><span data-stu-id="7df43-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="7df43-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7df43-104">SYNTAX</span></span>

### <span data-ttu-id="7df43-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7df43-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7df43-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="7df43-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df43-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7df43-107">DESCRIPTION</span></span>
<span data-ttu-id="7df43-108">Criar ou atualizar um resultado de avaliação de segurança em um recurso pode ser usado para alterar o status de um resultado existente ou adicionar dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="7df43-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="7df43-109">só pode ser usado para tipos de avaliação "CustomerManaged" e somente depois que os metadados de avaliação corresponderem são criados.</span><span class="sxs-lookup"><span data-stu-id="7df43-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="7df43-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7df43-110">EXAMPLES</span></span>

### <span data-ttu-id="7df43-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7df43-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="7df43-112">Marca o resultado da assinatura como "Não Ínteio" para avaliação do tipo "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - mais detalhes sobre o tipo de avaliação serão encontrados no tipo assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="7df43-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="7df43-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7df43-113">PARAMETERS</span></span>

### <span data-ttu-id="7df43-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="7df43-114">-AdditionalData</span></span>
<span data-ttu-id="7df43-115">Dados anexados ao resultado da avaliação para melhores investigações ou clareza de status.</span><span class="sxs-lookup"><span data-stu-id="7df43-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="7df43-116">-AssessedResourceId</span></span>
<span data-ttu-id="7df43-117">ID completa do recurso em que a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="7df43-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="7df43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df43-118">-DefaultProfile</span></span>
<span data-ttu-id="7df43-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7df43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7df43-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7df43-120">-Name</span></span>
<span data-ttu-id="7df43-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7df43-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="7df43-122">-StatusCause</span></span>
<span data-ttu-id="7df43-123">Código de progremmatic para a causa do resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="7df43-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7df43-124">-StatusCode</span></span>
<span data-ttu-id="7df43-125">Código progremático para o resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="7df43-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="7df43-126">pode ser "Healthy", "Unhealthy" ou "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="7df43-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="7df43-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="7df43-127">-StatusDescription</span></span>
<span data-ttu-id="7df43-128">Descrição acessível humana da causa do resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="7df43-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7df43-129">-Confirm</span></span>
<span data-ttu-id="7df43-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df43-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df43-131">-WhatIf</span></span>
<span data-ttu-id="7df43-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7df43-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df43-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7df43-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7df43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df43-134">CommonParameters</span></span>
<span data-ttu-id="7df43-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df43-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7df43-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df43-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7df43-137">INPUTS</span></span>

### <span data-ttu-id="7df43-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7df43-138">None</span></span>

## <span data-ttu-id="7df43-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7df43-139">OUTPUTS</span></span>

### <span data-ttu-id="7df43-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="7df43-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="7df43-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="7df43-141">NOTES</span></span>

## <span data-ttu-id="7df43-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7df43-142">RELATED LINKS</span></span>
