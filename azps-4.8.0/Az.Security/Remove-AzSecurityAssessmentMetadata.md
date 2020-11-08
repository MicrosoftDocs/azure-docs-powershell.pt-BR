---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113967"
---
# <span data-ttu-id="683ee-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="683ee-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="683ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="683ee-102">SYNOPSIS</span></span>
<span data-ttu-id="683ee-103">Exclui metadados de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="683ee-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="683ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="683ee-104">SYNTAX</span></span>

### <span data-ttu-id="683ee-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="683ee-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683ee-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="683ee-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683ee-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="683ee-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="683ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="683ee-108">DESCRIPTION</span></span>
<span data-ttu-id="683ee-109">Exclui metadados de avaliação de segurança de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="683ee-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="683ee-110">Esta ação excluirá o tipo de avaliação e todos os resultados de avaliação relevantes da assinatura.</span><span class="sxs-lookup"><span data-stu-id="683ee-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="683ee-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="683ee-111">EXAMPLES</span></span>

### <span data-ttu-id="683ee-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="683ee-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="683ee-113">Exclui um tipo de avaliação de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="683ee-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="683ee-114">OS</span><span class="sxs-lookup"><span data-stu-id="683ee-114">PARAMETERS</span></span>

### <span data-ttu-id="683ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683ee-115">-DefaultProfile</span></span>
<span data-ttu-id="683ee-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="683ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683ee-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="683ee-117">-InputObject</span></span>
<span data-ttu-id="683ee-118">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="683ee-118">Input Object.</span></span>

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

### <span data-ttu-id="683ee-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="683ee-119">-Name</span></span>
<span data-ttu-id="683ee-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="683ee-120">Resource name.</span></span>

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

### <span data-ttu-id="683ee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="683ee-121">-PassThru</span></span>
<span data-ttu-id="683ee-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="683ee-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="683ee-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="683ee-123">-ResourceId</span></span>
<span data-ttu-id="683ee-124">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="683ee-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="683ee-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="683ee-125">-Confirm</span></span>
<span data-ttu-id="683ee-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683ee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683ee-127">-WhatIf</span></span>
<span data-ttu-id="683ee-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="683ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683ee-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="683ee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683ee-130">CommonParameters</span></span>
<span data-ttu-id="683ee-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683ee-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="683ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683ee-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="683ee-133">INPUTS</span></span>

### <span data-ttu-id="683ee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="683ee-134">System.String</span></span>

### <span data-ttu-id="683ee-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="683ee-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="683ee-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="683ee-136">OUTPUTS</span></span>

### <span data-ttu-id="683ee-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="683ee-137">System.Boolean</span></span>

## <span data-ttu-id="683ee-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="683ee-138">NOTES</span></span>

## <span data-ttu-id="683ee-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="683ee-139">RELATED LINKS</span></span>
