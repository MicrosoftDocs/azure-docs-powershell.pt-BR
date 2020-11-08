---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110884"
---
# <span data-ttu-id="48bb0-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="48bb0-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="48bb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="48bb0-103">Cria ou atualiza um tipo de avaliação de segurança.</span><span class="sxs-lookup"><span data-stu-id="48bb0-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="48bb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48bb0-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48bb0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="48bb0-106">Cria ou atualiza metadados de avaliação de segurança, pode ser usado para criar e gerenciar várias propriedades de avaliação.</span><span class="sxs-lookup"><span data-stu-id="48bb0-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="48bb0-107">Depois dessa ação, você poderá relatar resultados de avaliação em qualquer recurso desta assinatura.</span><span class="sxs-lookup"><span data-stu-id="48bb0-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="48bb0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48bb0-108">EXAMPLES</span></span>

### <span data-ttu-id="48bb0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48bb0-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="48bb0-110">Criar um novo tipo de avaliação em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="48bb0-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="48bb0-111">OS</span><span class="sxs-lookup"><span data-stu-id="48bb0-111">PARAMETERS</span></span>

### <span data-ttu-id="48bb0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48bb0-112">-DefaultProfile</span></span>
<span data-ttu-id="48bb0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48bb0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48bb0-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="48bb0-114">-Description</span></span>
<span data-ttu-id="48bb0-115">Cadeia de caracteres detalhada que ajudará os usuários a entender o significado dessa avaliação e como ela foi calculada.</span><span class="sxs-lookup"><span data-stu-id="48bb0-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="48bb0-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="48bb0-116">-DisplayName</span></span>
<span data-ttu-id="48bb0-117">Título legível pelo homem para este objeto.</span><span class="sxs-lookup"><span data-stu-id="48bb0-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="48bb0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="48bb0-118">-Name</span></span>
<span data-ttu-id="48bb0-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="48bb0-119">Resource name.</span></span>

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

### <span data-ttu-id="48bb0-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="48bb0-120">-RemediationDescription</span></span>
<span data-ttu-id="48bb0-121">Cadeia de caracteres detalhada que ajudará os usuários a entender as diferentes maneiras de reduzir ou corrigir o problema de segurança.</span><span class="sxs-lookup"><span data-stu-id="48bb0-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="48bb0-122">-Severidade</span><span class="sxs-lookup"><span data-stu-id="48bb0-122">-Severity</span></span>
<span data-ttu-id="48bb0-123">Indica a importância do risco de segurança se a avaliação não estiver íntegra.</span><span class="sxs-lookup"><span data-stu-id="48bb0-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="48bb0-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48bb0-124">-Confirm</span></span>
<span data-ttu-id="48bb0-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48bb0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48bb0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48bb0-126">-WhatIf</span></span>
<span data-ttu-id="48bb0-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48bb0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48bb0-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48bb0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48bb0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48bb0-129">CommonParameters</span></span>
<span data-ttu-id="48bb0-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48bb0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48bb0-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48bb0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48bb0-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48bb0-132">INPUTS</span></span>

### <span data-ttu-id="48bb0-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="48bb0-133">None</span></span>

## <span data-ttu-id="48bb0-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48bb0-134">OUTPUTS</span></span>

### <span data-ttu-id="48bb0-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="48bb0-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="48bb0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48bb0-136">NOTES</span></span>

## <span data-ttu-id="48bb0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48bb0-137">RELATED LINKS</span></span>
