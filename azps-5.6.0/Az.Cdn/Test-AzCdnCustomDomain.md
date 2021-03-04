---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: b2c061f7755c7891946bcf8ea8f3fa5cdb15439d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889802"
---
# <span data-ttu-id="be368-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be368-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="be368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be368-102">SYNOPSIS</span></span>
<span data-ttu-id="be368-103">Verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="be368-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="be368-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="be368-104">SYNTAX</span></span>

### <span data-ttu-id="be368-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be368-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be368-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be368-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be368-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="be368-107">DESCRIPTION</span></span>
<span data-ttu-id="be368-108">O cmdlet **Test-AzCdnCustomDomain** verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade validando o mapeamento CName.</span><span class="sxs-lookup"><span data-stu-id="be368-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="be368-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be368-109">EXAMPLES</span></span>

## <span data-ttu-id="be368-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="be368-110">PARAMETERS</span></span>

### <span data-ttu-id="be368-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="be368-111">-CdnEndpoint</span></span>
<span data-ttu-id="be368-112">Especifica o ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="be368-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="be368-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="be368-113">-CustomDomainHostName</span></span>
<span data-ttu-id="be368-114">Especifica o nome de host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="be368-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="be368-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be368-115">-DefaultProfile</span></span>
<span data-ttu-id="be368-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be368-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be368-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="be368-117">-EndpointName</span></span>
<span data-ttu-id="be368-118">Especifica o nome do ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="be368-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="be368-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="be368-119">-ProfileName</span></span>
<span data-ttu-id="be368-120">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="be368-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="be368-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be368-121">-ResourceGroupName</span></span>
<span data-ttu-id="be368-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be368-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="be368-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be368-123">CommonParameters</span></span>
<span data-ttu-id="be368-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be368-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be368-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be368-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be368-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be368-126">INPUTS</span></span>

### <span data-ttu-id="be368-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="be368-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="be368-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="be368-128">OUTPUTS</span></span>

### <span data-ttu-id="be368-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="be368-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="be368-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="be368-130">NOTES</span></span>

## <span data-ttu-id="be368-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be368-131">RELATED LINKS</span></span>

[<span data-ttu-id="be368-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be368-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="be368-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be368-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="be368-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be368-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


