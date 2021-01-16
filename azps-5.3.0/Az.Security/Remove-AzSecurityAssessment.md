---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271539"
---
# <span data-ttu-id="a853d-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a853d-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="a853d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a853d-102">SYNOPSIS</span></span>
<span data-ttu-id="a853d-103">Exclui um resultado de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a853d-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="a853d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a853d-104">SYNTAX</span></span>

### <span data-ttu-id="a853d-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a853d-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853d-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="a853d-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853d-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a853d-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a853d-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="a853d-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a853d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a853d-109">DESCRIPTION</span></span>
<span data-ttu-id="a853d-110">Exclui um resultado de avaliação de segurança de uma assinatura, geralmente usado quando um resoruce é excluído ou quando a avaliação não é relevante para um recurso específico mais</span><span class="sxs-lookup"><span data-stu-id="a853d-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="a853d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a853d-111">EXAMPLES</span></span>

### <span data-ttu-id="a853d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a853d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="a853d-113">Exclui um resultado de avaliação em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a853d-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="a853d-114">OS</span><span class="sxs-lookup"><span data-stu-id="a853d-114">PARAMETERS</span></span>

### <span data-ttu-id="a853d-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a853d-115">-AssessedResourceId</span></span>
<span data-ttu-id="a853d-116">ID do recurso completo do recurso no qual a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="a853d-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="a853d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a853d-117">-DefaultProfile</span></span>
<span data-ttu-id="a853d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a853d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a853d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a853d-119">-InputObject</span></span>
<span data-ttu-id="a853d-120">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="a853d-120">Input Object.</span></span>

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

### <span data-ttu-id="a853d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a853d-121">-Name</span></span>
<span data-ttu-id="a853d-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a853d-122">Resource name.</span></span>

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

### <span data-ttu-id="a853d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a853d-123">-PassThru</span></span>
<span data-ttu-id="a853d-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a853d-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a853d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a853d-125">-ResourceId</span></span>
<span data-ttu-id="a853d-126">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="a853d-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a853d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a853d-127">-Confirm</span></span>
<span data-ttu-id="a853d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a853d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a853d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a853d-129">-WhatIf</span></span>
<span data-ttu-id="a853d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a853d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a853d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a853d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a853d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a853d-132">CommonParameters</span></span>
<span data-ttu-id="a853d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a853d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a853d-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a853d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a853d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a853d-135">INPUTS</span></span>

### <span data-ttu-id="a853d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a853d-136">System.String</span></span>

### <span data-ttu-id="a853d-137">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a853d-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a853d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a853d-138">OUTPUTS</span></span>

### <span data-ttu-id="a853d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a853d-139">System.Boolean</span></span>

## <span data-ttu-id="a853d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a853d-140">NOTES</span></span>

## <span data-ttu-id="a853d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a853d-141">RELATED LINKS</span></span>
