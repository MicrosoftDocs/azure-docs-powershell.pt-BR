---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431118"
---
# <span data-ttu-id="badeb-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="badeb-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="badeb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="badeb-102">SYNOPSIS</span></span>
<span data-ttu-id="badeb-103">Limpa um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="badeb-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="badeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="badeb-104">SYNTAX</span></span>

### <span data-ttu-id="badeb-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="badeb-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="badeb-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="badeb-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="badeb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="badeb-107">DESCRIPTION</span></span>
<span data-ttu-id="badeb-108">O cmdlet **UNPUBLISH-AzureRmCdnEndpointContent** limpa o conteúdo de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="badeb-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="badeb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="badeb-109">EXAMPLES</span></span>

## <span data-ttu-id="badeb-110">OS</span><span class="sxs-lookup"><span data-stu-id="badeb-110">PARAMETERS</span></span>

### <span data-ttu-id="badeb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="badeb-111">-CdnEndpoint</span></span>
<span data-ttu-id="badeb-112">Especifica o ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="badeb-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="badeb-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="badeb-113">-EndpointName</span></span>
<span data-ttu-id="badeb-114">Especifica o nome do ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="badeb-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badeb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="badeb-115">-PassThru</span></span>
<span data-ttu-id="badeb-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="badeb-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="badeb-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="badeb-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="badeb-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="badeb-118">-ProfileName</span></span>
<span data-ttu-id="badeb-119">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="badeb-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badeb-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="badeb-120">-PurgeContent</span></span>
<span data-ttu-id="badeb-121">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="badeb-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="badeb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="badeb-122">-ResourceGroupName</span></span>
<span data-ttu-id="badeb-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="badeb-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="badeb-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="badeb-124">-Confirm</span></span>
<span data-ttu-id="badeb-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="badeb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="badeb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="badeb-126">-WhatIf</span></span>
<span data-ttu-id="badeb-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="badeb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="badeb-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="badeb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="badeb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badeb-129">-DefaultProfile</span></span>
<span data-ttu-id="badeb-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="badeb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="badeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badeb-131">CommonParameters</span></span>
<span data-ttu-id="badeb-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="badeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badeb-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="badeb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badeb-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="badeb-134">INPUTS</span></span>

### <span data-ttu-id="badeb-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="badeb-135">PSEndpoint</span></span>
<span data-ttu-id="badeb-136">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="badeb-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="badeb-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="badeb-137">OUTPUTS</span></span>

### <span data-ttu-id="badeb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="badeb-138">System.Boolean</span></span>

## <span data-ttu-id="badeb-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="badeb-139">NOTES</span></span>

## <span data-ttu-id="badeb-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="badeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="badeb-141">Publicar-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="badeb-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


