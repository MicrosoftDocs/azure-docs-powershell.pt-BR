---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: ff69cd6296dbd95f959beb48fef6e496866e54f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893113"
---
# <span data-ttu-id="d4233-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d4233-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="d4233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4233-102">SYNOPSIS</span></span>
<span data-ttu-id="d4233-103">Exclui um resultado de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d4233-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="d4233-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d4233-104">SYNTAX</span></span>

### <span data-ttu-id="d4233-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4233-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4233-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="d4233-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4233-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4233-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4233-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4233-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4233-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d4233-109">DESCRIPTION</span></span>
<span data-ttu-id="d4233-110">Exclui um resultado de avaliação de segurança de uma assinatura, geralmente usada quando uma resoruce é excluída ou quando a avaliação não é mais relevante para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="d4233-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="d4233-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4233-111">EXAMPLES</span></span>

### <span data-ttu-id="d4233-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4233-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="d4233-113">Exclui um resultado de avaliação em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d4233-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="d4233-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d4233-114">PARAMETERS</span></span>

### <span data-ttu-id="d4233-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="d4233-115">-AssessedResourceId</span></span>
<span data-ttu-id="d4233-116">ID completa do recurso em que a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="d4233-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4233-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4233-117">-DefaultProfile</span></span>
<span data-ttu-id="d4233-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4233-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4233-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4233-119">-InputObject</span></span>
<span data-ttu-id="d4233-120">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="d4233-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4233-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4233-121">-Name</span></span>
<span data-ttu-id="d4233-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d4233-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4233-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4233-123">-PassThru</span></span>
<span data-ttu-id="d4233-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d4233-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4233-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4233-125">-ResourceId</span></span>
<span data-ttu-id="d4233-126">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="d4233-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d4233-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4233-127">-Confirm</span></span>
<span data-ttu-id="d4233-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4233-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4233-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4233-129">-WhatIf</span></span>
<span data-ttu-id="d4233-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4233-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4233-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4233-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4233-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4233-132">CommonParameters</span></span>
<span data-ttu-id="d4233-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4233-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4233-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4233-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4233-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4233-135">INPUTS</span></span>

### <span data-ttu-id="d4233-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d4233-136">System.String</span></span>

### <span data-ttu-id="d4233-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d4233-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="d4233-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d4233-138">OUTPUTS</span></span>

### <span data-ttu-id="d4233-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4233-139">System.Boolean</span></span>

## <span data-ttu-id="d4233-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="d4233-140">NOTES</span></span>

## <span data-ttu-id="d4233-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4233-141">RELATED LINKS</span></span>
