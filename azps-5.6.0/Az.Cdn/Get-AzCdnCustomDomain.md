---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: e1c436a76a3fc98714798bc938f0de987906e7d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893004"
---
# <span data-ttu-id="b70d7-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b70d7-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="b70d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b70d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b70d7-103">Obtém um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="b70d7-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="b70d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b70d7-104">SYNTAX</span></span>

### <span data-ttu-id="b70d7-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b70d7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b70d7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b70d7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70d7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b70d7-107">DESCRIPTION</span></span>
<span data-ttu-id="b70d7-108">O cmdlet **Get-AzCdnCustomDomain** obtém um domínio personalizado da Rede de Entrega de Conteúdo (CDN) do Azure e suas configurações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b70d7-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="b70d7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b70d7-109">EXAMPLES</span></span>

## <span data-ttu-id="b70d7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b70d7-110">PARAMETERS</span></span>

### <span data-ttu-id="b70d7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b70d7-111">-CdnEndpoint</span></span>
<span data-ttu-id="b70d7-112">Especifica o objeto de ponto de extremidade CDN do qual o domínio personalizado é membro.</span><span class="sxs-lookup"><span data-stu-id="b70d7-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="b70d7-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b70d7-113">-CustomDomainName</span></span>
<span data-ttu-id="b70d7-114">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="b70d7-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="b70d7-115">O nome do domínio personalizado difere do nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="b70d7-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70d7-116">-DefaultProfile</span></span>
<span data-ttu-id="b70d7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b70d7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b70d7-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b70d7-118">-EndpointName</span></span>
<span data-ttu-id="b70d7-119">Especifica o nome do ponto de extremidade ao qual o domínio personalizado pertence.</span><span class="sxs-lookup"><span data-stu-id="b70d7-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b70d7-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b70d7-120">-ProfileName</span></span>
<span data-ttu-id="b70d7-121">Especifica o nome do Perfil ao qual o domínio personalizado pertence.</span><span class="sxs-lookup"><span data-stu-id="b70d7-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b70d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b70d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="b70d7-123">Especifica o nome do grupo de recursos ao qual o domínio personalizado pertence.</span><span class="sxs-lookup"><span data-stu-id="b70d7-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b70d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70d7-124">CommonParameters</span></span>
<span data-ttu-id="b70d7-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70d7-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b70d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b70d7-127">INPUTS</span></span>

### <span data-ttu-id="b70d7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b70d7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b70d7-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b70d7-129">OUTPUTS</span></span>

### <span data-ttu-id="b70d7-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b70d7-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="b70d7-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="b70d7-131">NOTES</span></span>

## <span data-ttu-id="b70d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b70d7-132">RELATED LINKS</span></span>

[<span data-ttu-id="b70d7-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b70d7-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="b70d7-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b70d7-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


