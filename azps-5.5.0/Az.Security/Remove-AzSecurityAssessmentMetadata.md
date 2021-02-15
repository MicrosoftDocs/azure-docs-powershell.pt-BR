---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118704"
---
# <span data-ttu-id="9104e-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9104e-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9104e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9104e-102">SYNOPSIS</span></span>
<span data-ttu-id="9104e-103">Exclui metadados de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9104e-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="9104e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9104e-104">SYNTAX</span></span>

### <span data-ttu-id="9104e-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9104e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9104e-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="9104e-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9104e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9104e-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9104e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9104e-108">DESCRIPTION</span></span>
<span data-ttu-id="9104e-109">Exclui metadados de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="9104e-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="9104e-110">Essa ação excluirá o tipo de avaliação e todos os resultados de avaliação relevantes da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9104e-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="9104e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9104e-111">EXAMPLES</span></span>

### <span data-ttu-id="9104e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9104e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="9104e-113">Exclui um tipo de avaliação de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="9104e-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="9104e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9104e-114">PARAMETERS</span></span>

### <span data-ttu-id="9104e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9104e-115">-DefaultProfile</span></span>
<span data-ttu-id="9104e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9104e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9104e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9104e-117">-InputObject</span></span>
<span data-ttu-id="9104e-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9104e-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9104e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9104e-119">-Name</span></span>
<span data-ttu-id="9104e-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9104e-120">Resource name.</span></span>

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

### <span data-ttu-id="9104e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9104e-121">-PassThru</span></span>
<span data-ttu-id="9104e-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9104e-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9104e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9104e-123">-ResourceId</span></span>
<span data-ttu-id="9104e-124">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="9104e-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9104e-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9104e-125">-Confirm</span></span>
<span data-ttu-id="9104e-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9104e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9104e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9104e-127">-WhatIf</span></span>
<span data-ttu-id="9104e-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9104e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9104e-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9104e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9104e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9104e-130">CommonParameters</span></span>
<span data-ttu-id="9104e-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9104e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9104e-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9104e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9104e-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="9104e-133">INPUTS</span></span>

### <span data-ttu-id="9104e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9104e-134">System.String</span></span>

### <span data-ttu-id="9104e-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="9104e-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="9104e-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="9104e-136">OUTPUTS</span></span>

### <span data-ttu-id="9104e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9104e-137">System.Boolean</span></span>

## <span data-ttu-id="9104e-138">Notas</span><span class="sxs-lookup"><span data-stu-id="9104e-138">NOTES</span></span>

## <span data-ttu-id="9104e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9104e-139">RELATED LINKS</span></span>
