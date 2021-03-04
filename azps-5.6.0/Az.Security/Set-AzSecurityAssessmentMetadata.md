---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: e72766e754394bb43775f73072941dc0d3989c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889743"
---
# <span data-ttu-id="084f2-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="084f2-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="084f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="084f2-102">SYNOPSIS</span></span>
<span data-ttu-id="084f2-103">Cria ou atualiza um tipo de avaliação de segurança.</span><span class="sxs-lookup"><span data-stu-id="084f2-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="084f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="084f2-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="084f2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="084f2-105">DESCRIPTION</span></span>
<span data-ttu-id="084f2-106">Cria ou atualiza metadados de avaliação de segurança, pode ser usado para criar e gerenciar várias propriedades de avaliação.</span><span class="sxs-lookup"><span data-stu-id="084f2-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="084f2-107">Após essa ação, você poderá relatar os resultados da avaliação em qualquer recurso desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="084f2-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="084f2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="084f2-108">EXAMPLES</span></span>

### <span data-ttu-id="084f2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="084f2-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="084f2-110">Crie um novo tipo de avaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="084f2-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="084f2-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="084f2-111">PARAMETERS</span></span>

### <span data-ttu-id="084f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084f2-112">-DefaultProfile</span></span>
<span data-ttu-id="084f2-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="084f2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084f2-114">-Description</span><span class="sxs-lookup"><span data-stu-id="084f2-114">-Description</span></span>
<span data-ttu-id="084f2-115">Cadeia de caracteres detalhada que ajudará os usuários a entender o significado dessa avaliação e como ela foi calculada.</span><span class="sxs-lookup"><span data-stu-id="084f2-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="084f2-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="084f2-116">-DisplayName</span></span>
<span data-ttu-id="084f2-117">Título acessível para humanos para este objeto.</span><span class="sxs-lookup"><span data-stu-id="084f2-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="084f2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="084f2-118">-Name</span></span>
<span data-ttu-id="084f2-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="084f2-119">Resource name.</span></span>

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

### <span data-ttu-id="084f2-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="084f2-120">-RemediationDescription</span></span>
<span data-ttu-id="084f2-121">Cadeia de caracteres detalhada que ajudará os usuários a entender as diferentes maneiras de mitigar ou corrigir o problema de segurança.</span><span class="sxs-lookup"><span data-stu-id="084f2-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="084f2-122">-Severity</span><span class="sxs-lookup"><span data-stu-id="084f2-122">-Severity</span></span>
<span data-ttu-id="084f2-123">Indica a importância do risco de segurança se a avaliação não for saudável.</span><span class="sxs-lookup"><span data-stu-id="084f2-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="084f2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="084f2-124">-Confirm</span></span>
<span data-ttu-id="084f2-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="084f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084f2-126">-WhatIf</span></span>
<span data-ttu-id="084f2-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="084f2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084f2-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="084f2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084f2-129">CommonParameters</span></span>
<span data-ttu-id="084f2-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084f2-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="084f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084f2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="084f2-132">INPUTS</span></span>

### <span data-ttu-id="084f2-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="084f2-133">None</span></span>

## <span data-ttu-id="084f2-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="084f2-134">OUTPUTS</span></span>

### <span data-ttu-id="084f2-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="084f2-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="084f2-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="084f2-136">NOTES</span></span>

## <span data-ttu-id="084f2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="084f2-137">RELATED LINKS</span></span>
