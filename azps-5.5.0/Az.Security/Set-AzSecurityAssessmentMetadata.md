---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118690"
---
# <span data-ttu-id="2f664-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2f664-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2f664-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f664-102">SYNOPSIS</span></span>
<span data-ttu-id="2f664-103">Cria ou atualiza um tipo de avaliação de segurança.</span><span class="sxs-lookup"><span data-stu-id="2f664-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="2f664-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f664-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f664-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f664-105">DESCRIPTION</span></span>
<span data-ttu-id="2f664-106">Cria ou atualiza metadados de avaliação de segurança, que podem ser usados para criar e gerenciar várias propriedades de avaliação.</span><span class="sxs-lookup"><span data-stu-id="2f664-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="2f664-107">Após essa ação, você poderá relatar os resultados da avaliação em qualquer recurso desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="2f664-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="2f664-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f664-108">EXAMPLES</span></span>

### <span data-ttu-id="2f664-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f664-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="2f664-110">Crie um novo tipo de avaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="2f664-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="2f664-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f664-111">PARAMETERS</span></span>

### <span data-ttu-id="2f664-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f664-112">-DefaultProfile</span></span>
<span data-ttu-id="2f664-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f664-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f664-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="2f664-114">-Description</span></span>
<span data-ttu-id="2f664-115">Cadeia de caracteres detalhada que ajudará os usuários a entender o significado dessa avaliação e como ela foi calculada.</span><span class="sxs-lookup"><span data-stu-id="2f664-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="2f664-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f664-116">-DisplayName</span></span>
<span data-ttu-id="2f664-117">Título acessível para este objeto.</span><span class="sxs-lookup"><span data-stu-id="2f664-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="2f664-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f664-118">-Name</span></span>
<span data-ttu-id="2f664-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2f664-119">Resource name.</span></span>

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

### <span data-ttu-id="2f664-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="2f664-120">-RemediationDescription</span></span>
<span data-ttu-id="2f664-121">Cadeia de caracteres detalhada que ajudará os usuários a entender as diferentes maneiras de mitigar ou corrigir o problema de segurança.</span><span class="sxs-lookup"><span data-stu-id="2f664-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="2f664-122">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="2f664-122">-Severity</span></span>
<span data-ttu-id="2f664-123">Indica a importância do risco de segurança se a avaliação não for saudável.</span><span class="sxs-lookup"><span data-stu-id="2f664-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="2f664-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2f664-124">-Confirm</span></span>
<span data-ttu-id="2f664-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f664-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f664-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f664-126">-WhatIf</span></span>
<span data-ttu-id="2f664-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2f664-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f664-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f664-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f664-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f664-129">CommonParameters</span></span>
<span data-ttu-id="2f664-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f664-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f664-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f664-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f664-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="2f664-132">INPUTS</span></span>

### <span data-ttu-id="2f664-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f664-133">None</span></span>

## <span data-ttu-id="2f664-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="2f664-134">OUTPUTS</span></span>

### <span data-ttu-id="2f664-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="2f664-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="2f664-136">Notas</span><span class="sxs-lookup"><span data-stu-id="2f664-136">NOTES</span></span>

## <span data-ttu-id="2f664-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f664-137">RELATED LINKS</span></span>
