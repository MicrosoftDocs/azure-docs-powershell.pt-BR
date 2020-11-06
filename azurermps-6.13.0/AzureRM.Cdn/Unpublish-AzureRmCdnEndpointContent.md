---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 15ab6c6974924458e6a206dac3d3629f3f4c48a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609411"
---
# <span data-ttu-id="60144-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="60144-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="60144-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60144-102">SYNOPSIS</span></span>
<span data-ttu-id="60144-103">Limpa um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="60144-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60144-104">SYNTAX</span></span>

### <span data-ttu-id="60144-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="60144-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60144-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60144-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60144-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60144-107">DESCRIPTION</span></span>
<span data-ttu-id="60144-108">O cmdlet **UNPUBLISH-AzureRmCdnEndpointContent** limpa o conteúdo de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="60144-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="60144-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60144-109">EXAMPLES</span></span>

## <span data-ttu-id="60144-110">OS</span><span class="sxs-lookup"><span data-stu-id="60144-110">PARAMETERS</span></span>

### <span data-ttu-id="60144-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60144-111">-CdnEndpoint</span></span>
<span data-ttu-id="60144-112">Especifica o ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="60144-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="60144-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60144-113">-DefaultProfile</span></span>
<span data-ttu-id="60144-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60144-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60144-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="60144-115">-EndpointName</span></span>
<span data-ttu-id="60144-116">Especifica o nome do ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="60144-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="60144-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60144-117">-PassThru</span></span>
<span data-ttu-id="60144-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="60144-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60144-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="60144-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60144-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="60144-120">-ProfileName</span></span>
<span data-ttu-id="60144-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="60144-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="60144-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="60144-122">-PurgeContent</span></span>
<span data-ttu-id="60144-123">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="60144-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="60144-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60144-124">-ResourceGroupName</span></span>
<span data-ttu-id="60144-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="60144-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="60144-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60144-126">-Confirm</span></span>
<span data-ttu-id="60144-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60144-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60144-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60144-128">-WhatIf</span></span>
<span data-ttu-id="60144-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60144-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60144-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60144-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60144-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60144-131">CommonParameters</span></span>
<span data-ttu-id="60144-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60144-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60144-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60144-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60144-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60144-134">INPUTS</span></span>

### <span data-ttu-id="60144-135">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="60144-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="60144-136">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60144-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="60144-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60144-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60144-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60144-138">OUTPUTS</span></span>

### <span data-ttu-id="60144-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60144-139">System.Boolean</span></span>

## <span data-ttu-id="60144-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60144-140">NOTES</span></span>

## <span data-ttu-id="60144-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60144-141">RELATED LINKS</span></span>

[<span data-ttu-id="60144-142">Publicar-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="60144-142">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


