---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427181"
---
# <span data-ttu-id="4be66-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="4be66-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="4be66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4be66-102">SYNOPSIS</span></span>
<span data-ttu-id="4be66-103">Criar ou atualizar um resultado da avaliação de segurança em um recurso</span><span class="sxs-lookup"><span data-stu-id="4be66-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="4be66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4be66-104">SYNTAX</span></span>

### <span data-ttu-id="4be66-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4be66-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4be66-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="4be66-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4be66-107">DESCRIPTION</span></span>
<span data-ttu-id="4be66-108">Criar ou atualizar um resultado de avaliação de segurança em um recurso, pode ser usado para alterar o status de um resultado existente ou adicionar dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="4be66-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="4be66-109">Só pode ser usado para tipos de avaliação "CustomerManaged" e somente após a criação dos metadados de avaliação correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4be66-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="4be66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4be66-110">EXAMPLES</span></span>

### <span data-ttu-id="4be66-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4be66-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="4be66-112">Marca o resultado da assinatura como "não íntegro" para avaliação do tipo "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D"-mais detalhes sobre o tipo de avaliação serão encontrados sob o tipo assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="4be66-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="4be66-113">OS</span><span class="sxs-lookup"><span data-stu-id="4be66-113">PARAMETERS</span></span>

### <span data-ttu-id="4be66-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="4be66-114">-AdditionalData</span></span>
<span data-ttu-id="4be66-115">Dados anexados ao resultado da avaliação para obter melhores investigações ou maior clareza do status.</span><span class="sxs-lookup"><span data-stu-id="4be66-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

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

### <span data-ttu-id="4be66-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="4be66-116">-AssessedResourceId</span></span>
<span data-ttu-id="4be66-117">ID do recurso completo do recurso no qual a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="4be66-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="4be66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be66-118">-DefaultProfile</span></span>
<span data-ttu-id="4be66-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4be66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be66-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4be66-120">-Name</span></span>
<span data-ttu-id="4be66-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4be66-121">Resource name.</span></span>

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

### <span data-ttu-id="4be66-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="4be66-122">-StatusCause</span></span>
<span data-ttu-id="4be66-123">Progremmatic código para a causa do resultado da apuração.</span><span class="sxs-lookup"><span data-stu-id="4be66-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="4be66-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4be66-124">-StatusCode</span></span>
<span data-ttu-id="4be66-125">Progremmatic código do resultado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="4be66-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="4be66-126">pode ser "íntegro", "não íntegro" ou "não aplicável"</span><span class="sxs-lookup"><span data-stu-id="4be66-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

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

### <span data-ttu-id="4be66-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="4be66-127">-StatusDescription</span></span>
<span data-ttu-id="4be66-128">Descrição da causa do resultado da apuração humanamente legível.</span><span class="sxs-lookup"><span data-stu-id="4be66-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="4be66-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4be66-129">-Confirm</span></span>
<span data-ttu-id="4be66-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4be66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be66-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be66-131">-WhatIf</span></span>
<span data-ttu-id="4be66-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4be66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be66-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4be66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be66-134">CommonParameters</span></span>
<span data-ttu-id="4be66-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be66-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4be66-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be66-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4be66-137">INPUTS</span></span>

### <span data-ttu-id="4be66-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4be66-138">None</span></span>

## <span data-ttu-id="4be66-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4be66-139">OUTPUTS</span></span>

### <span data-ttu-id="4be66-140">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="4be66-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="4be66-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4be66-141">NOTES</span></span>

## <span data-ttu-id="4be66-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4be66-142">RELATED LINKS</span></span>
