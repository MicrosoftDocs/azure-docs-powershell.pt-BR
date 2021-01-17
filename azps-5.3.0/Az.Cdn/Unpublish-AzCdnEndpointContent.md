---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430308"
---
# <span data-ttu-id="c854a-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="c854a-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="c854a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c854a-102">SYNOPSIS</span></span>
<span data-ttu-id="c854a-103">Limpa um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="c854a-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="c854a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c854a-104">SYNTAX</span></span>

### <span data-ttu-id="c854a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c854a-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c854a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c854a-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c854a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c854a-107">DESCRIPTION</span></span>
<span data-ttu-id="c854a-108">O cmdlet **UNPUBLISH-AzCdnEndpointContent** limpa o conteúdo de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="c854a-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c854a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c854a-109">EXAMPLES</span></span>

## <span data-ttu-id="c854a-110">OS</span><span class="sxs-lookup"><span data-stu-id="c854a-110">PARAMETERS</span></span>

### <span data-ttu-id="c854a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c854a-111">-CdnEndpoint</span></span>
<span data-ttu-id="c854a-112">Especifica o ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="c854a-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="c854a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c854a-113">-DefaultProfile</span></span>
<span data-ttu-id="c854a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c854a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c854a-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c854a-115">-EndpointName</span></span>
<span data-ttu-id="c854a-116">Especifica o nome do ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="c854a-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="c854a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c854a-117">-PassThru</span></span>
<span data-ttu-id="c854a-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c854a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c854a-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c854a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c854a-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c854a-120">-ProfileName</span></span>
<span data-ttu-id="c854a-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="c854a-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c854a-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="c854a-122">-PurgeContent</span></span>
<span data-ttu-id="c854a-123">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="c854a-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="c854a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c854a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c854a-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="c854a-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="c854a-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c854a-126">-Confirm</span></span>
<span data-ttu-id="c854a-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c854a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c854a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c854a-128">-WhatIf</span></span>
<span data-ttu-id="c854a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c854a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c854a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c854a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c854a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c854a-131">CommonParameters</span></span>
<span data-ttu-id="c854a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c854a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c854a-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c854a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c854a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c854a-134">INPUTS</span></span>

### <span data-ttu-id="c854a-135">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c854a-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="c854a-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c854a-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c854a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c854a-137">OUTPUTS</span></span>

### <span data-ttu-id="c854a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c854a-138">System.Boolean</span></span>

## <span data-ttu-id="c854a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c854a-139">NOTES</span></span>

## <span data-ttu-id="c854a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c854a-140">RELATED LINKS</span></span>

[<span data-ttu-id="c854a-141">Publicar-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="c854a-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


