---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 82d980768147bb82332dae2dfa8965d962cc882e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885888"
---
# <span data-ttu-id="4ac38-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4ac38-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4ac38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ac38-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac38-103">Habilita HTTPS de domínio personalizado (preterido).</span><span class="sxs-lookup"><span data-stu-id="4ac38-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="4ac38-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ac38-104">SYNTAX</span></span>

### <span data-ttu-id="4ac38-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ac38-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ac38-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac38-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ac38-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ac38-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac38-108">O cmdlet **Enable-AzCdnCustomDomain** habilita a entrega HTTPS segura de um domínio personalizado cdn.</span><span class="sxs-lookup"><span data-stu-id="4ac38-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="4ac38-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ac38-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac38-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ac38-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="4ac38-111">Habilitar a entrega https do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ac38-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="4ac38-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ac38-112">PARAMETERS</span></span>

### <span data-ttu-id="4ac38-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4ac38-113">-CustomDomainName</span></span>
<span data-ttu-id="4ac38-114">Nome de exibição de domínio personalizado do Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4ac38-114">Azure CDN custom domain display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac38-115">-DefaultProfile</span></span>
<span data-ttu-id="4ac38-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac38-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4ac38-117">-EndpointName</span></span>
<span data-ttu-id="4ac38-118">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac38-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ac38-119">-InputObject</span></span>
<span data-ttu-id="4ac38-120">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ac38-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ac38-121">-PassThru</span></span>
<span data-ttu-id="4ac38-122">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="4ac38-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4ac38-123">-ProfileName</span></span>
<span data-ttu-id="4ac38-124">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac38-124">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac38-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ac38-126">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac38-126">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ac38-127">-Confirm</span></span>
<span data-ttu-id="4ac38-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac38-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac38-129">-WhatIf</span></span>
<span data-ttu-id="4ac38-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ac38-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac38-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ac38-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac38-132">CommonParameters</span></span>
<span data-ttu-id="4ac38-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac38-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ac38-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac38-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ac38-135">INPUTS</span></span>

### <span data-ttu-id="4ac38-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4ac38-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4ac38-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ac38-137">OUTPUTS</span></span>

### <span data-ttu-id="4ac38-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ac38-138">System.Boolean</span></span>

## <span data-ttu-id="4ac38-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ac38-139">NOTES</span></span>

## <span data-ttu-id="4ac38-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ac38-140">RELATED LINKS</span></span>
