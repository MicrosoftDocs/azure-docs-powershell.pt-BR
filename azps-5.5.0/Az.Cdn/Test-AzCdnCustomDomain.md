---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115502"
---
# <span data-ttu-id="2aea5-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2aea5-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2aea5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2aea5-102">SYNOPSIS</span></span>
<span data-ttu-id="2aea5-103">Verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2aea5-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="2aea5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aea5-104">SYNTAX</span></span>

### <span data-ttu-id="2aea5-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2aea5-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aea5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aea5-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aea5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2aea5-107">DESCRIPTION</span></span>
<span data-ttu-id="2aea5-108">O cmdlet **Test-AzCdnCustomDomain** verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade validando o mapeamento CName.</span><span class="sxs-lookup"><span data-stu-id="2aea5-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="2aea5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2aea5-109">EXAMPLES</span></span>

## <span data-ttu-id="2aea5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aea5-110">PARAMETERS</span></span>

### <span data-ttu-id="2aea5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2aea5-111">-CdnEndpoint</span></span>
<span data-ttu-id="2aea5-112">Especifica o ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="2aea5-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="2aea5-113">-CustomDomainHostName</span></span>
<span data-ttu-id="2aea5-114">Especifica o nome de host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="2aea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aea5-115">-DefaultProfile</span></span>
<span data-ttu-id="2aea5-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2aea5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aea5-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="2aea5-117">-EndpointName</span></span>
<span data-ttu-id="2aea5-118">Especifica o nome do ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="2aea5-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2aea5-119">-ProfileName</span></span>
<span data-ttu-id="2aea5-120">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="2aea5-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="2aea5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aea5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2aea5-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2aea5-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2aea5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aea5-123">CommonParameters</span></span>
<span data-ttu-id="2aea5-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aea5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aea5-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2aea5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aea5-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="2aea5-126">INPUTS</span></span>

### <span data-ttu-id="2aea5-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2aea5-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2aea5-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="2aea5-128">OUTPUTS</span></span>

### <span data-ttu-id="2aea5-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="2aea5-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="2aea5-130">Notas</span><span class="sxs-lookup"><span data-stu-id="2aea5-130">NOTES</span></span>

## <span data-ttu-id="2aea5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aea5-131">RELATED LINKS</span></span>

[<span data-ttu-id="2aea5-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2aea5-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="2aea5-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2aea5-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="2aea5-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2aea5-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


