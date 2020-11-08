---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113970"
---
# <span data-ttu-id="5078c-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5078c-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="5078c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5078c-102">SYNOPSIS</span></span>
<span data-ttu-id="5078c-103">Exclui um resultado de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5078c-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="5078c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5078c-104">SYNTAX</span></span>

### <span data-ttu-id="5078c-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="5078c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5078c-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="5078c-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5078c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="5078c-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5078c-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5078c-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5078c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5078c-109">DESCRIPTION</span></span>
<span data-ttu-id="5078c-110">Exclui um resultado de avaliação de segurança de uma assinatura, geralmente usado quando um resoruce é excluído ou quando a avaliação não é relevante para um recurso específico mais</span><span class="sxs-lookup"><span data-stu-id="5078c-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="5078c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5078c-111">EXAMPLES</span></span>

### <span data-ttu-id="5078c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5078c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="5078c-113">Exclui um resultado de avaliação em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="5078c-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="5078c-114">OS</span><span class="sxs-lookup"><span data-stu-id="5078c-114">PARAMETERS</span></span>

### <span data-ttu-id="5078c-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="5078c-115">-AssessedResourceId</span></span>
<span data-ttu-id="5078c-116">ID do recurso completo do recurso no qual a avaliação é calculada.</span><span class="sxs-lookup"><span data-stu-id="5078c-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="5078c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5078c-117">-DefaultProfile</span></span>
<span data-ttu-id="5078c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5078c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5078c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5078c-119">-InputObject</span></span>
<span data-ttu-id="5078c-120">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="5078c-120">Input Object.</span></span>

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

### <span data-ttu-id="5078c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5078c-121">-Name</span></span>
<span data-ttu-id="5078c-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5078c-122">Resource name.</span></span>

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

### <span data-ttu-id="5078c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5078c-123">-PassThru</span></span>
<span data-ttu-id="5078c-124">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5078c-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5078c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5078c-125">-ResourceId</span></span>
<span data-ttu-id="5078c-126">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="5078c-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5078c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5078c-127">-Confirm</span></span>
<span data-ttu-id="5078c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5078c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5078c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5078c-129">-WhatIf</span></span>
<span data-ttu-id="5078c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5078c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5078c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5078c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5078c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5078c-132">CommonParameters</span></span>
<span data-ttu-id="5078c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5078c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5078c-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5078c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5078c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5078c-135">INPUTS</span></span>

### <span data-ttu-id="5078c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5078c-136">System.String</span></span>

### <span data-ttu-id="5078c-137">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5078c-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="5078c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5078c-138">OUTPUTS</span></span>

### <span data-ttu-id="5078c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5078c-139">System.Boolean</span></span>

## <span data-ttu-id="5078c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5078c-140">NOTES</span></span>

## <span data-ttu-id="5078c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5078c-141">RELATED LINKS</span></span>
