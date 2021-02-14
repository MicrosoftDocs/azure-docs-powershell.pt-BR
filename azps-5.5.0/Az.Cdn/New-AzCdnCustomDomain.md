---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116582"
---
# <span data-ttu-id="f20b3-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f20b3-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f20b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f20b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f20b3-103">Cria um domínio personalizado para um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="f20b3-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="f20b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f20b3-104">SYNTAX</span></span>

### <span data-ttu-id="f20b3-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f20b3-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20b3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f20b3-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20b3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f20b3-107">DESCRIPTION</span></span>
<span data-ttu-id="f20b3-108">O cmdlet **New-AzCdnCustomDomain** cria um domínio personalizado para o ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="f20b3-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f20b3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f20b3-109">EXAMPLES</span></span>

## <span data-ttu-id="f20b3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f20b3-110">PARAMETERS</span></span>

### <span data-ttu-id="f20b3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f20b3-111">-CdnEndpoint</span></span>
<span data-ttu-id="f20b3-112">Especifica o objeto do ponto de extremidade CDN ao qual o domínio personalizado é adicionado.</span><span class="sxs-lookup"><span data-stu-id="f20b3-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="f20b3-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f20b3-113">-CustomDomainName</span></span>
<span data-ttu-id="f20b3-114">Especifica o nome do recurso do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="f20b3-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="f20b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20b3-115">-DefaultProfile</span></span>
<span data-ttu-id="f20b3-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f20b3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f20b3-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="f20b3-117">-EndpointName</span></span>
<span data-ttu-id="f20b3-118">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f20b3-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="f20b3-119">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="f20b3-119">-HostName</span></span>
<span data-ttu-id="f20b3-120">Especifica o nome de host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="f20b3-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f20b3-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f20b3-121">-ProfileName</span></span>
<span data-ttu-id="f20b3-122">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="f20b3-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f20b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f20b3-124">Especifica o nome do grupo de recursos ao qual o domínio personalizado pertence.</span><span class="sxs-lookup"><span data-stu-id="f20b3-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f20b3-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f20b3-125">-Confirm</span></span>
<span data-ttu-id="f20b3-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f20b3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20b3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20b3-127">-WhatIf</span></span>
<span data-ttu-id="f20b3-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f20b3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20b3-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f20b3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20b3-130">CommonParameters</span></span>
<span data-ttu-id="f20b3-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f20b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20b3-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f20b3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20b3-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f20b3-133">INPUTS</span></span>

### <span data-ttu-id="f20b3-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f20b3-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f20b3-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="f20b3-135">OUTPUTS</span></span>

### <span data-ttu-id="f20b3-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f20b3-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="f20b3-137">Notas</span><span class="sxs-lookup"><span data-stu-id="f20b3-137">NOTES</span></span>

## <span data-ttu-id="f20b3-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f20b3-138">RELATED LINKS</span></span>

[<span data-ttu-id="f20b3-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f20b3-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="f20b3-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f20b3-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="f20b3-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f20b3-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


