---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940332"
---
# <span data-ttu-id="6b658-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="6b658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b658-102">SYNOPSIS</span></span>
<span data-ttu-id="6b658-103">Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b658-103">Removes a custom domain.</span></span>

## <span data-ttu-id="6b658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b658-104">SYNTAX</span></span>

### <span data-ttu-id="6b658-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b658-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b658-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b658-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b658-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b658-107">DESCRIPTION</span></span>
<span data-ttu-id="6b658-108">O cmdlet **Remove-AzCdnCustomDomain** remove o domínio personalizado de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b658-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6b658-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b658-109">EXAMPLES</span></span>

## <span data-ttu-id="6b658-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b658-110">PARAMETERS</span></span>

### <span data-ttu-id="6b658-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-111">-CdnCustomDomain</span></span>
<span data-ttu-id="6b658-112">Especifica o domínio personalizado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6b658-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b658-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6b658-113">-CustomDomainName</span></span>
<span data-ttu-id="6b658-114">Especifica o nome do recurso do domínio personalizado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="6b658-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6b658-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b658-115">-DefaultProfile</span></span>
<span data-ttu-id="6b658-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b658-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b658-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b658-117">-EndpointName</span></span>
<span data-ttu-id="6b658-118">Especifica o nome do ponto de extremidade do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b658-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b658-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b658-119">-PassThru</span></span>
<span data-ttu-id="6b658-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6b658-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b658-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6b658-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b658-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6b658-122">-ProfileName</span></span>
<span data-ttu-id="6b658-123">Especifica o nome do perfil do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b658-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b658-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b658-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b658-125">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b658-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6b658-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6b658-126">-Confirm</span></span>
<span data-ttu-id="6b658-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b658-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b658-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b658-128">-WhatIf</span></span>
<span data-ttu-id="6b658-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b658-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b658-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b658-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b658-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b658-131">CommonParameters</span></span>
<span data-ttu-id="6b658-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b658-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b658-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b658-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b658-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b658-134">INPUTS</span></span>

### <span data-ttu-id="6b658-135">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="6b658-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b658-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b658-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b658-137">OUTPUTS</span></span>

### <span data-ttu-id="6b658-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b658-138">System.Boolean</span></span>

## <span data-ttu-id="6b658-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b658-139">NOTES</span></span>

## <span data-ttu-id="6b658-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b658-140">RELATED LINKS</span></span>

[<span data-ttu-id="6b658-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="6b658-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="6b658-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b658-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


