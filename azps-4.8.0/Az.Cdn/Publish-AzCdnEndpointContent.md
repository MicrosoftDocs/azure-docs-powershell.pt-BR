---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955083"
---
# <span data-ttu-id="58d34-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="58d34-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="58d34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58d34-102">SYNOPSIS</span></span>
<span data-ttu-id="58d34-103">Carrega o conteúdo em um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="58d34-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="58d34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58d34-104">SYNTAX</span></span>

### <span data-ttu-id="58d34-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="58d34-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58d34-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58d34-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d34-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58d34-107">DESCRIPTION</span></span>
<span data-ttu-id="58d34-108">O cmdlet **Publish-AzCdnEndpointContent** carrega o conteúdo de um servidor de origem para o ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="58d34-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="58d34-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58d34-109">EXAMPLES</span></span>

## <span data-ttu-id="58d34-110">OS</span><span class="sxs-lookup"><span data-stu-id="58d34-110">PARAMETERS</span></span>

### <span data-ttu-id="58d34-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d34-111">-CdnEndpoint</span></span>
<span data-ttu-id="58d34-112">Especifica o ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="58d34-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="58d34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d34-113">-DefaultProfile</span></span>
<span data-ttu-id="58d34-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58d34-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58d34-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="58d34-115">-EndpointName</span></span>
<span data-ttu-id="58d34-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="58d34-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="58d34-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="58d34-117">-LoadContent</span></span>
<span data-ttu-id="58d34-118">Especifica uma matriz de caminhos relativos para o conteúdo do servidor de origem que esse cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="58d34-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="58d34-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58d34-119">-PassThru</span></span>
<span data-ttu-id="58d34-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="58d34-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58d34-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="58d34-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58d34-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="58d34-122">-ProfileName</span></span>
<span data-ttu-id="58d34-123">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="58d34-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="58d34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d34-124">-ResourceGroupName</span></span>
<span data-ttu-id="58d34-125">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="58d34-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="58d34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d34-126">CommonParameters</span></span>
<span data-ttu-id="58d34-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d34-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58d34-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d34-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58d34-129">INPUTS</span></span>

### <span data-ttu-id="58d34-130">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="58d34-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="58d34-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58d34-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58d34-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58d34-132">OUTPUTS</span></span>

### <span data-ttu-id="58d34-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58d34-133">System.Boolean</span></span>

## <span data-ttu-id="58d34-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58d34-134">NOTES</span></span>

## <span data-ttu-id="58d34-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58d34-135">RELATED LINKS</span></span>

[<span data-ttu-id="58d34-136">Cancelar publicação-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="58d34-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)


