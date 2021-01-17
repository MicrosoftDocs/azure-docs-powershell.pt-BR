---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434441"
---
# <span data-ttu-id="cc948-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="cc948-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="cc948-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc948-102">SYNOPSIS</span></span>
<span data-ttu-id="cc948-103">Obtém um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="cc948-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="cc948-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc948-104">SYNTAX</span></span>

### <span data-ttu-id="cc948-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc948-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc948-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc948-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc948-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc948-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc948-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc948-108">DESCRIPTION</span></span>
<span data-ttu-id="cc948-109">O cmdlet **Get-AzCdnOrigin** Obtém um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="cc948-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="cc948-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc948-110">EXAMPLES</span></span>

## <span data-ttu-id="cc948-111">OS</span><span class="sxs-lookup"><span data-stu-id="cc948-111">PARAMETERS</span></span>

### <span data-ttu-id="cc948-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc948-112">-CdnEndpoint</span></span>
<span data-ttu-id="cc948-113">Especifica o objeto de ponto de extremidade CDN ao qual a origem pertence.</span><span class="sxs-lookup"><span data-stu-id="cc948-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="cc948-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc948-114">-DefaultProfile</span></span>
<span data-ttu-id="cc948-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cc948-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc948-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cc948-116">-EndpointName</span></span>
<span data-ttu-id="cc948-117">Especifica o nome do ponto de extremidade ao qual pertence o servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="cc948-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="cc948-118">-Originname</span><span class="sxs-lookup"><span data-stu-id="cc948-118">-OriginName</span></span>
<span data-ttu-id="cc948-119">Especifica o nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="cc948-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="cc948-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cc948-120">-ProfileName</span></span>
<span data-ttu-id="cc948-121">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="cc948-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="cc948-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc948-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc948-123">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="cc948-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="cc948-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc948-124">-ResourceId</span></span>
<span data-ttu-id="cc948-125">A ID do recurso da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc948-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc948-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc948-126">CommonParameters</span></span>
<span data-ttu-id="cc948-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc948-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc948-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc948-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc948-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc948-129">INPUTS</span></span>

### <span data-ttu-id="cc948-130">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc948-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cc948-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc948-131">OUTPUTS</span></span>

### <span data-ttu-id="cc948-132">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="cc948-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="cc948-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc948-133">NOTES</span></span>

## <span data-ttu-id="cc948-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc948-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc948-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="cc948-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


