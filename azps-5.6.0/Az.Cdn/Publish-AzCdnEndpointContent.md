---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 73d5c679e1079f99cc19f2af6c22e2d5b5a491fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891510"
---
# <span data-ttu-id="11f4d-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="11f4d-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="11f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="11f4d-103">Carrega conteúdo para um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11f4d-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="11f4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11f4d-104">SYNTAX</span></span>

### <span data-ttu-id="11f4d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11f4d-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11f4d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11f4d-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f4d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11f4d-107">DESCRIPTION</span></span>
<span data-ttu-id="11f4d-108">O cmdlet **Publish-AzCdnEndpointContent** carrega conteúdo de um servidor de origem para o ponto de extremidade cdn (Rede de Distribuição de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="11f4d-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="11f4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11f4d-109">EXAMPLES</span></span>

## <span data-ttu-id="11f4d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="11f4d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="11f4d-111">-CdnEndpoint</span></span>
<span data-ttu-id="11f4d-112">Especifica o ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="11f4d-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="11f4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f4d-113">-DefaultProfile</span></span>
<span data-ttu-id="11f4d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="11f4d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11f4d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="11f4d-115">-EndpointName</span></span>
<span data-ttu-id="11f4d-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="11f4d-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="11f4d-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="11f4d-117">-LoadContent</span></span>
<span data-ttu-id="11f4d-118">Especifica uma matriz de caminhos relativos para o conteúdo no servidor de origem que este cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="11f4d-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f4d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11f4d-119">-PassThru</span></span>
<span data-ttu-id="11f4d-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="11f4d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="11f4d-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="11f4d-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f4d-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="11f4d-122">-ProfileName</span></span>
<span data-ttu-id="11f4d-123">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="11f4d-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="11f4d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f4d-124">-ResourceGroupName</span></span>
<span data-ttu-id="11f4d-125">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="11f4d-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="11f4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f4d-126">CommonParameters</span></span>
<span data-ttu-id="11f4d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f4d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11f4d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f4d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11f4d-129">INPUTS</span></span>

### <span data-ttu-id="11f4d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="11f4d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="11f4d-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11f4d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11f4d-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11f4d-132">OUTPUTS</span></span>

### <span data-ttu-id="11f4d-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11f4d-133">System.Boolean</span></span>

## <span data-ttu-id="11f4d-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="11f4d-134">NOTES</span></span>

## <span data-ttu-id="11f4d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11f4d-135">RELATED LINKS</span></span>

[<span data-ttu-id="11f4d-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="11f4d-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


