---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 4fe845225d2d396849e398f6974b1addf854d393
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601409"
---
# <span data-ttu-id="c8d57-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c8d57-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c8d57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8d57-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d57-103">Cria um domínio personalizado para um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="c8d57-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="c8d57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8d57-104">SYNTAX</span></span>

### <span data-ttu-id="c8d57-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8d57-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8d57-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8d57-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8d57-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8d57-107">DESCRIPTION</span></span>
<span data-ttu-id="c8d57-108">O cmdlet **New-AzCdnCustomDomain** cria um domínio personalizado para o ponto de extremidade da rede de distribuição de conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8d57-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c8d57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8d57-109">EXAMPLES</span></span>

## <span data-ttu-id="c8d57-110">OS</span><span class="sxs-lookup"><span data-stu-id="c8d57-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d57-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8d57-111">-CdnEndpoint</span></span>
<span data-ttu-id="c8d57-112">Especifica o objeto de ponto de extremidade CDN ao qual o domínio personalizado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d57-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c8d57-113">-CustomDomainName</span></span>
<span data-ttu-id="c8d57-114">Especifica o nome do recurso do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d57-115">-DefaultProfile</span></span>
<span data-ttu-id="c8d57-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c8d57-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8d57-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c8d57-117">-EndpointName</span></span>
<span data-ttu-id="c8d57-118">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c8d57-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="c8d57-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="c8d57-119">-HostName</span></span>
<span data-ttu-id="c8d57-120">Especifica o nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d57-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c8d57-121">-ProfileName</span></span>
<span data-ttu-id="c8d57-122">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="c8d57-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="c8d57-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d57-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8d57-124">Especifica o nome do grupo de recursos ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="c8d57-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8d57-125">-Confirm</span></span>
<span data-ttu-id="c8d57-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8d57-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d57-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d57-127">-WhatIf</span></span>
<span data-ttu-id="c8d57-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d57-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8d57-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d57-130">CommonParameters</span></span>
<span data-ttu-id="c8d57-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d57-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d57-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d57-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8d57-133">INPUTS</span></span>

### <span data-ttu-id="c8d57-134">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c8d57-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c8d57-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8d57-135">OUTPUTS</span></span>

### <span data-ttu-id="c8d57-136">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c8d57-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c8d57-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8d57-137">NOTES</span></span>

## <span data-ttu-id="c8d57-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8d57-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8d57-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c8d57-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="c8d57-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c8d57-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="c8d57-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c8d57-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


