---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116924"
---
# <span data-ttu-id="5abd7-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="5abd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5abd7-102">SYNOPSIS</span></span>
<span data-ttu-id="5abd7-103">Obtém um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="5abd7-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="5abd7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5abd7-104">SYNTAX</span></span>

### <span data-ttu-id="5abd7-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5abd7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5abd7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5abd7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5abd7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5abd7-107">DESCRIPTION</span></span>
<span data-ttu-id="5abd7-108">O cmdlet **Get-AzCdnEndpoint** obtém um ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure e seus dados de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="5abd7-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="5abd7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5abd7-109">EXAMPLES</span></span>

## <span data-ttu-id="5abd7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5abd7-110">PARAMETERS</span></span>

### <span data-ttu-id="5abd7-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5abd7-111">-CdnProfile</span></span>
<span data-ttu-id="5abd7-112">Especifica o objeto de perfil cdn ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="5abd7-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5abd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abd7-113">-DefaultProfile</span></span>
<span data-ttu-id="5abd7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5abd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5abd7-115">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="5abd7-115">-EndpointName</span></span>
<span data-ttu-id="5abd7-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5abd7-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="5abd7-117">O nome do ponto de extremidade não é o nome de host do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5abd7-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="5abd7-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5abd7-118">-ProfileName</span></span>
<span data-ttu-id="5abd7-119">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="5abd7-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5abd7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5abd7-120">-ResourceGroupName</span></span>
<span data-ttu-id="5abd7-121">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="5abd7-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5abd7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abd7-122">CommonParameters</span></span>
<span data-ttu-id="5abd7-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5abd7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abd7-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5abd7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abd7-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="5abd7-125">INPUTS</span></span>

### <span data-ttu-id="5abd7-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="5abd7-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5abd7-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="5abd7-127">OUTPUTS</span></span>

### <span data-ttu-id="5abd7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5abd7-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5abd7-129">NOTES</span></span>

## <span data-ttu-id="5abd7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5abd7-130">RELATED LINKS</span></span>

[<span data-ttu-id="5abd7-131">Novo-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="5abd7-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="5abd7-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="5abd7-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="5abd7-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5abd7-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


