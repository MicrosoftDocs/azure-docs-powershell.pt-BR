---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432791"
---
# <span data-ttu-id="827af-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="827af-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="827af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="827af-102">SYNOPSIS</span></span>
<span data-ttu-id="827af-103">Verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="827af-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="827af-104">SYNTAX</span></span>

### <span data-ttu-id="827af-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="827af-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="827af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="827af-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="827af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="827af-107">DESCRIPTION</span></span>
<span data-ttu-id="827af-108">O cmdlet **Test-AzureRmCdnCustomDomain** verifica se um domínio personalizado pode ser adicionado a um ponto de extremidade Validando o mapeamento CNAME.</span><span class="sxs-lookup"><span data-stu-id="827af-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="827af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="827af-109">EXAMPLES</span></span>

## <span data-ttu-id="827af-110">OS</span><span class="sxs-lookup"><span data-stu-id="827af-110">PARAMETERS</span></span>

### <span data-ttu-id="827af-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="827af-111">-CdnEndpoint</span></span>
<span data-ttu-id="827af-112">Especifica o ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="827af-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="827af-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="827af-113">-CustomDomainHostName</span></span>
<span data-ttu-id="827af-114">Especifica o nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="827af-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="827af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827af-115">-DefaultProfile</span></span>
<span data-ttu-id="827af-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="827af-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="827af-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="827af-117">-EndpointName</span></span>
<span data-ttu-id="827af-118">Especifica o nome do ponto de extremidade ao qual você deseja adicionar o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="827af-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="827af-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="827af-119">-ProfileName</span></span>
<span data-ttu-id="827af-120">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="827af-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="827af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827af-121">-ResourceGroupName</span></span>
<span data-ttu-id="827af-122">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="827af-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="827af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827af-123">CommonParameters</span></span>
<span data-ttu-id="827af-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827af-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827af-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="827af-126">INPUTS</span></span>

### <span data-ttu-id="827af-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="827af-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="827af-128">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="827af-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="827af-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="827af-129">OUTPUTS</span></span>

### <span data-ttu-id="827af-130">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="827af-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="827af-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="827af-131">NOTES</span></span>

## <span data-ttu-id="827af-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="827af-132">RELATED LINKS</span></span>

[<span data-ttu-id="827af-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="827af-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="827af-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="827af-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="827af-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="827af-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


