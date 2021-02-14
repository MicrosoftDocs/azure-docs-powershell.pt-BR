---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115513"
---
# <span data-ttu-id="d780f-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d780f-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d780f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d780f-102">SYNOPSIS</span></span>
<span data-ttu-id="d780f-103">Habilita o HTTPS de domínio personalizado (preterido).</span><span class="sxs-lookup"><span data-stu-id="d780f-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="d780f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d780f-104">SYNTAX</span></span>

### <span data-ttu-id="d780f-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d780f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d780f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d780f-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d780f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d780f-107">DESCRIPTION</span></span>
<span data-ttu-id="d780f-108">O cmdlet **Enable-AzCdnCustomDomain** habilita a entrega HTTPS protegida de um domínio personalizado de CDN.</span><span class="sxs-lookup"><span data-stu-id="d780f-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d780f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d780f-109">EXAMPLES</span></span>

### <span data-ttu-id="d780f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d780f-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="d780f-111">Habilitar a entrega https do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d780f-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="d780f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d780f-112">PARAMETERS</span></span>

### <span data-ttu-id="d780f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d780f-113">-CustomDomainName</span></span>
<span data-ttu-id="d780f-114">Nome de exibição de domínio personalizado cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="d780f-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d780f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d780f-115">-DefaultProfile</span></span>
<span data-ttu-id="d780f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d780f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d780f-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="d780f-117">-EndpointName</span></span>
<span data-ttu-id="d780f-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="d780f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d780f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d780f-119">-InputObject</span></span>
<span data-ttu-id="d780f-120">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d780f-120">The custom domain object.</span></span>

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

### <span data-ttu-id="d780f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d780f-121">-PassThru</span></span>
<span data-ttu-id="d780f-122">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="d780f-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="d780f-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d780f-123">-ProfileName</span></span>
<span data-ttu-id="d780f-124">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="d780f-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d780f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d780f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d780f-126">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="d780f-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d780f-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d780f-127">-Confirm</span></span>
<span data-ttu-id="d780f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d780f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d780f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d780f-129">-WhatIf</span></span>
<span data-ttu-id="d780f-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d780f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d780f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d780f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d780f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d780f-132">CommonParameters</span></span>
<span data-ttu-id="d780f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d780f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d780f-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d780f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d780f-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="d780f-135">INPUTS</span></span>

### <span data-ttu-id="d780f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d780f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d780f-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d780f-137">OUTPUTS</span></span>

### <span data-ttu-id="d780f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d780f-138">System.Boolean</span></span>

## <span data-ttu-id="d780f-139">Notas</span><span class="sxs-lookup"><span data-stu-id="d780f-139">NOTES</span></span>

## <span data-ttu-id="d780f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d780f-140">RELATED LINKS</span></span>
