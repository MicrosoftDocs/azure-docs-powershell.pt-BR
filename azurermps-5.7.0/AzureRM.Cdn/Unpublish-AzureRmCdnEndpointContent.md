---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: bb55b858e4c2464cced362357ffbc91a3969b1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431079"
---
# <span data-ttu-id="f1b68-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f1b68-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="f1b68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b68-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b68-103">Limpa um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="f1b68-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b68-104">SYNTAX</span></span>

### <span data-ttu-id="f1b68-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1b68-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1b68-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1b68-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1b68-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1b68-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b68-108">O cmdlet **UNPUBLISH-AzureRmCdnEndpointContent** limpa o conteúdo de um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b68-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f1b68-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1b68-109">EXAMPLES</span></span>

## <span data-ttu-id="f1b68-110">OS</span><span class="sxs-lookup"><span data-stu-id="f1b68-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b68-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1b68-111">-CdnEndpoint</span></span>
<span data-ttu-id="f1b68-112">Especifica o ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="f1b68-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b68-113">-DefaultProfile</span></span>
<span data-ttu-id="f1b68-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f1b68-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f1b68-115">-EndpointName</span></span>
<span data-ttu-id="f1b68-116">Especifica o nome do ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="f1b68-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b68-117">-PassThru</span></span>
<span data-ttu-id="f1b68-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f1b68-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1b68-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f1b68-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f1b68-120">-ProfileName</span></span>
<span data-ttu-id="f1b68-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="f1b68-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="f1b68-122">-PurgeContent</span></span>
<span data-ttu-id="f1b68-123">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="f1b68-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b68-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1b68-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="f1b68-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1b68-126">-Confirm</span></span>
<span data-ttu-id="f1b68-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b68-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b68-128">-WhatIf</span></span>
<span data-ttu-id="f1b68-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1b68-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b68-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1b68-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b68-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b68-131">CommonParameters</span></span>
<span data-ttu-id="f1b68-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b68-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b68-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b68-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b68-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1b68-134">INPUTS</span></span>

### <span data-ttu-id="f1b68-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1b68-135">PSEndpoint</span></span>
<span data-ttu-id="f1b68-136">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f1b68-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f1b68-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1b68-137">OUTPUTS</span></span>

### <span data-ttu-id="f1b68-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1b68-138">System.Boolean</span></span>

## <span data-ttu-id="f1b68-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1b68-139">NOTES</span></span>

## <span data-ttu-id="f1b68-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b68-140">RELATED LINKS</span></span>

[<span data-ttu-id="f1b68-141">Publicar-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="f1b68-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


