---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116908"
---
# <span data-ttu-id="d28c9-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d28c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d28c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d28c9-103">Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-103">Removes a custom domain.</span></span>

## <span data-ttu-id="d28c9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d28c9-104">SYNTAX</span></span>

### <span data-ttu-id="d28c9-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d28c9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d28c9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d28c9-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d28c9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d28c9-107">DESCRIPTION</span></span>
<span data-ttu-id="d28c9-108">O cmdlet **Remove-AzCdnCustomDomain** remove o domínio personalizado de um ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="d28c9-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d28c9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d28c9-109">EXAMPLES</span></span>

## <span data-ttu-id="d28c9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d28c9-110">PARAMETERS</span></span>

### <span data-ttu-id="d28c9-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-111">-CdnCustomDomain</span></span>
<span data-ttu-id="d28c9-112">Especifica o domínio personalizado que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d28c9-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d28c9-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d28c9-113">-CustomDomainName</span></span>
<span data-ttu-id="d28c9-114">Especifica o nome do recurso do domínio personalizado que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d28c9-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d28c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28c9-115">-DefaultProfile</span></span>
<span data-ttu-id="d28c9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d28c9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d28c9-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="d28c9-117">-EndpointName</span></span>
<span data-ttu-id="d28c9-118">Especifica o nome do ponto de extremidade do qual este cmdlet remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d28c9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d28c9-119">-PassThru</span></span>
<span data-ttu-id="d28c9-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d28c9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d28c9-121">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="d28c9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d28c9-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d28c9-122">-ProfileName</span></span>
<span data-ttu-id="d28c9-123">Especifica o nome do perfil do qual este cmdlet remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d28c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d28c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d28c9-125">Especifica o nome do grupo de recursos do qual este cmdlet remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="d28c9-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d28c9-126">-Confirm</span></span>
<span data-ttu-id="d28c9-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d28c9-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d28c9-128">-WhatIf</span></span>
<span data-ttu-id="d28c9-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d28c9-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d28c9-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d28c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28c9-131">CommonParameters</span></span>
<span data-ttu-id="d28c9-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d28c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28c9-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d28c9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28c9-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="d28c9-134">INPUTS</span></span>

### <span data-ttu-id="d28c9-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d28c9-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d28c9-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d28c9-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d28c9-137">OUTPUTS</span></span>

### <span data-ttu-id="d28c9-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d28c9-138">System.Boolean</span></span>

## <span data-ttu-id="d28c9-139">Notas</span><span class="sxs-lookup"><span data-stu-id="d28c9-139">NOTES</span></span>

## <span data-ttu-id="d28c9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d28c9-140">RELATED LINKS</span></span>

[<span data-ttu-id="d28c9-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="d28c9-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="d28c9-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d28c9-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


