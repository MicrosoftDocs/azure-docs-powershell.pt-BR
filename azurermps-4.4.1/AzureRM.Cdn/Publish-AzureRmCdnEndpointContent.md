---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432653"
---
# <span data-ttu-id="17f1b-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="17f1b-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="17f1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="17f1b-103">Carrega o conteúdo em um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="17f1b-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17f1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17f1b-104">SYNTAX</span></span>

### <span data-ttu-id="17f1b-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="17f1b-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f1b-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="17f1b-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f1b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="17f1b-108">O cmdlet **Publish-AzureRmCdnEndpointContent** carrega o conteúdo de um servidor de origem para o ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f1b-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="17f1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17f1b-109">EXAMPLES</span></span>

## <span data-ttu-id="17f1b-110">OS</span><span class="sxs-lookup"><span data-stu-id="17f1b-110">PARAMETERS</span></span>

### <span data-ttu-id="17f1b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="17f1b-111">-CdnEndpoint</span></span>
<span data-ttu-id="17f1b-112">Sepcifies o ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="17f1b-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="17f1b-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="17f1b-113">-EndpointName</span></span>
<span data-ttu-id="17f1b-114">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="17f1b-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="17f1b-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="17f1b-115">-LoadContent</span></span>
<span data-ttu-id="17f1b-116">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que esse cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="17f1b-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="17f1b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17f1b-117">-PassThru</span></span>
<span data-ttu-id="17f1b-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="17f1b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17f1b-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="17f1b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17f1b-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="17f1b-120">-ProfileName</span></span>
<span data-ttu-id="17f1b-121">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="17f1b-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="17f1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="17f1b-123">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="17f1b-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="17f1b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f1b-124">-DefaultProfile</span></span>
<span data-ttu-id="17f1b-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17f1b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f1b-126">CommonParameters</span></span>
<span data-ttu-id="17f1b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f1b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f1b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17f1b-129">INPUTS</span></span>

### <span data-ttu-id="17f1b-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="17f1b-130">PSEndpoint</span></span>
<span data-ttu-id="17f1b-131">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="17f1b-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="17f1b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17f1b-132">OUTPUTS</span></span>

### <span data-ttu-id="17f1b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17f1b-133">System.Boolean</span></span>

## <span data-ttu-id="17f1b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17f1b-134">NOTES</span></span>

## <span data-ttu-id="17f1b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17f1b-135">RELATED LINKS</span></span>

[<span data-ttu-id="17f1b-136">Cancelar publicação-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="17f1b-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


