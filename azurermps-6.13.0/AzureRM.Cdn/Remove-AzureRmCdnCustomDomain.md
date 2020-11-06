---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431387"
---
# <span data-ttu-id="11c00-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="11c00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11c00-102">SYNOPSIS</span></span>
<span data-ttu-id="11c00-103">Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="11c00-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11c00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11c00-104">SYNTAX</span></span>

### <span data-ttu-id="11c00-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="11c00-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11c00-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c00-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c00-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11c00-107">DESCRIPTION</span></span>
<span data-ttu-id="11c00-108">O cmdlet **Remove-AzureRmCdnCustomDomain** remove o domínio personalizado de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="11c00-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="11c00-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11c00-109">EXAMPLES</span></span>

## <span data-ttu-id="11c00-110">OS</span><span class="sxs-lookup"><span data-stu-id="11c00-110">PARAMETERS</span></span>

### <span data-ttu-id="11c00-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-111">-CdnCustomDomain</span></span>
<span data-ttu-id="11c00-112">Especifica o domínio personalizado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="11c00-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="11c00-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="11c00-113">-CustomDomainName</span></span>
<span data-ttu-id="11c00-114">Especifica o nome do recurso do domínio personalizado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="11c00-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="11c00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c00-115">-DefaultProfile</span></span>
<span data-ttu-id="11c00-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="11c00-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11c00-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="11c00-117">-EndpointName</span></span>
<span data-ttu-id="11c00-118">Especifica o nome do ponto de extremidade do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="11c00-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="11c00-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11c00-119">-PassThru</span></span>
<span data-ttu-id="11c00-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="11c00-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11c00-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="11c00-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11c00-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="11c00-122">-ProfileName</span></span>
<span data-ttu-id="11c00-123">Especifica o nome do perfil do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="11c00-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="11c00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c00-124">-ResourceGroupName</span></span>
<span data-ttu-id="11c00-125">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="11c00-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="11c00-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11c00-126">-Confirm</span></span>
<span data-ttu-id="11c00-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c00-128">-WhatIf</span></span>
<span data-ttu-id="11c00-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11c00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c00-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11c00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c00-131">CommonParameters</span></span>
<span data-ttu-id="11c00-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c00-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c00-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c00-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11c00-134">INPUTS</span></span>

### <span data-ttu-id="11c00-135">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="11c00-136">Parâmetros: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11c00-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="11c00-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11c00-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11c00-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11c00-138">OUTPUTS</span></span>

### <span data-ttu-id="11c00-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11c00-139">System.Boolean</span></span>

## <span data-ttu-id="11c00-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11c00-140">NOTES</span></span>

## <span data-ttu-id="11c00-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11c00-141">RELATED LINKS</span></span>

[<span data-ttu-id="11c00-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="11c00-143">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="11c00-144">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c00-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


