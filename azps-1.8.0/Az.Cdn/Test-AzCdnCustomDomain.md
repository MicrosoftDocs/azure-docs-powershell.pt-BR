---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 3ab4e9c673ebea17bbf15d4f978f7c500660060a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771264"
---
# <span data-ttu-id="0d1d9-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d1d9-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="0d1d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1d9-103">Verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="0d1d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d1d9-104">SYNTAX</span></span>

### <span data-ttu-id="0d1d9-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d1d9-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d1d9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d1d9-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d1d9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d1d9-107">DESCRIPTION</span></span>
<span data-ttu-id="0d1d9-108">O cmdlet **Test-AzCdnCustomDomain** verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade Validando o mapeamento CNAME.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="0d1d9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d1d9-109">EXAMPLES</span></span>

## <span data-ttu-id="0d1d9-110">OS</span><span class="sxs-lookup"><span data-stu-id="0d1d9-110">PARAMETERS</span></span>

### <span data-ttu-id="0d1d9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d1d9-111">-CdnEndpoint</span></span>
<span data-ttu-id="0d1d9-112">Especifica o ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="0d1d9-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="0d1d9-113">-CustomDomainHostName</span></span>
<span data-ttu-id="0d1d9-114">Especifica o nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="0d1d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1d9-115">-DefaultProfile</span></span>
<span data-ttu-id="0d1d9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0d1d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d1d9-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0d1d9-117">-EndpointName</span></span>
<span data-ttu-id="0d1d9-118">Especifica o nome do ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="0d1d9-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0d1d9-119">-ProfileName</span></span>
<span data-ttu-id="0d1d9-120">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0d1d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d1d9-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0d1d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1d9-123">CommonParameters</span></span>
<span data-ttu-id="0d1d9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1d9-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1d9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1d9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d1d9-126">INPUTS</span></span>

### <span data-ttu-id="0d1d9-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d1d9-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0d1d9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d1d9-128">OUTPUTS</span></span>

### <span data-ttu-id="0d1d9-129">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="0d1d9-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="0d1d9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d1d9-130">NOTES</span></span>

## <span data-ttu-id="0d1d9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d1d9-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d1d9-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d1d9-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="0d1d9-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d1d9-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="0d1d9-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d1d9-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


