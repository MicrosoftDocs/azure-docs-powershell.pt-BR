---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112435"
---
# <span data-ttu-id="db00a-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="db00a-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="db00a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db00a-102">SYNOPSIS</span></span>
<span data-ttu-id="db00a-103">Obtém um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="db00a-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="db00a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db00a-104">SYNTAX</span></span>

### <span data-ttu-id="db00a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db00a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db00a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db00a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db00a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db00a-107">DESCRIPTION</span></span>
<span data-ttu-id="db00a-108">O cmdlet **Get-AzCdnOrigin** Obtém um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="db00a-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="db00a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db00a-109">EXAMPLES</span></span>

## <span data-ttu-id="db00a-110">OS</span><span class="sxs-lookup"><span data-stu-id="db00a-110">PARAMETERS</span></span>

### <span data-ttu-id="db00a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db00a-111">-CdnEndpoint</span></span>
<span data-ttu-id="db00a-112">Especifica o objeto de ponto de extremidade CDN ao qual a origem pertence.</span><span class="sxs-lookup"><span data-stu-id="db00a-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="db00a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db00a-113">-DefaultProfile</span></span>
<span data-ttu-id="db00a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db00a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db00a-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="db00a-115">-EndpointName</span></span>
<span data-ttu-id="db00a-116">Especifica o nome do ponto de extremidade ao qual pertence o servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db00a-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="db00a-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="db00a-117">-OriginName</span></span>
<span data-ttu-id="db00a-118">Especifica o nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db00a-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="db00a-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="db00a-119">-ProfileName</span></span>
<span data-ttu-id="db00a-120">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="db00a-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="db00a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db00a-121">-ResourceGroupName</span></span>
<span data-ttu-id="db00a-122">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="db00a-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="db00a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db00a-123">CommonParameters</span></span>
<span data-ttu-id="db00a-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db00a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db00a-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db00a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db00a-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db00a-126">INPUTS</span></span>

### <span data-ttu-id="db00a-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="db00a-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="db00a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db00a-128">OUTPUTS</span></span>

### <span data-ttu-id="db00a-129">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="db00a-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="db00a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db00a-130">NOTES</span></span>

## <span data-ttu-id="db00a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db00a-131">RELATED LINKS</span></span>

[<span data-ttu-id="db00a-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="db00a-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


