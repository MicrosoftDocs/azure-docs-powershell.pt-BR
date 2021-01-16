---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261311"
---
# <span data-ttu-id="45b24-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="45b24-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="45b24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45b24-102">SYNOPSIS</span></span>
<span data-ttu-id="45b24-103">Obtém um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="45b24-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="45b24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45b24-104">SYNTAX</span></span>

### <span data-ttu-id="45b24-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="45b24-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45b24-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45b24-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45b24-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45b24-107">DESCRIPTION</span></span>
<span data-ttu-id="45b24-108">O cmdlet **Get-AzCdnCustomDomain** Obtém um domínio personalizado de CDN (rede de distribuição de conteúdo) do Azure e suas configurações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="45b24-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="45b24-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45b24-109">EXAMPLES</span></span>

## <span data-ttu-id="45b24-110">OS</span><span class="sxs-lookup"><span data-stu-id="45b24-110">PARAMETERS</span></span>

### <span data-ttu-id="45b24-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="45b24-111">-CdnEndpoint</span></span>
<span data-ttu-id="45b24-112">Especifica o objeto de ponto de extremidade CDN do qual o domínio personalizado é membro.</span><span class="sxs-lookup"><span data-stu-id="45b24-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="45b24-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="45b24-113">-CustomDomainName</span></span>
<span data-ttu-id="45b24-114">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45b24-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="45b24-115">O nome do domínio personalizado é diferente do nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45b24-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="45b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b24-116">-DefaultProfile</span></span>
<span data-ttu-id="45b24-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="45b24-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45b24-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="45b24-118">-EndpointName</span></span>
<span data-ttu-id="45b24-119">Especifica o nome do ponto de extremidade ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45b24-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="45b24-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="45b24-120">-ProfileName</span></span>
<span data-ttu-id="45b24-121">Especifica o nome do perfil ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45b24-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="45b24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b24-122">-ResourceGroupName</span></span>
<span data-ttu-id="45b24-123">Especifica o nome do grupo de recursos ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45b24-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="45b24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b24-124">CommonParameters</span></span>
<span data-ttu-id="45b24-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b24-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b24-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b24-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45b24-127">INPUTS</span></span>

### <span data-ttu-id="45b24-128">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="45b24-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="45b24-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45b24-129">OUTPUTS</span></span>

### <span data-ttu-id="45b24-130">Microsoft. Azure. Commands. cdn. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="45b24-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="45b24-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45b24-131">NOTES</span></span>

## <span data-ttu-id="45b24-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45b24-132">RELATED LINKS</span></span>

[<span data-ttu-id="45b24-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="45b24-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="45b24-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="45b24-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


