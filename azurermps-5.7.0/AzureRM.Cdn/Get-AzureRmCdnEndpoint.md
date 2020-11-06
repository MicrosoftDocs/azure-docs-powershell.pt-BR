---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427658"
---
# <span data-ttu-id="e19b2-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e19b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e19b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e19b2-103">Obtém um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="e19b2-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e19b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e19b2-104">SYNTAX</span></span>

### <span data-ttu-id="e19b2-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e19b2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e19b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e19b2-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e19b2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e19b2-107">DESCRIPTION</span></span>
<span data-ttu-id="e19b2-108">O cmdlet **Get-AzureRMCdnEndpoint** Obtém um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="e19b2-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="e19b2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e19b2-109">EXAMPLES</span></span>

## <span data-ttu-id="e19b2-110">OS</span><span class="sxs-lookup"><span data-stu-id="e19b2-110">PARAMETERS</span></span>

### <span data-ttu-id="e19b2-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e19b2-111">-CdnProfile</span></span>
<span data-ttu-id="e19b2-112">Especifica o objeto de perfil CDN ao qual pertence o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e19b2-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e19b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19b2-113">-DefaultProfile</span></span>
<span data-ttu-id="e19b2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e19b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e19b2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e19b2-115">-EndpointName</span></span>
<span data-ttu-id="e19b2-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e19b2-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="e19b2-117">O nome do ponto de extremidade não é o nome de host do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e19b2-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e19b2-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e19b2-118">-ProfileName</span></span>
<span data-ttu-id="e19b2-119">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="e19b2-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e19b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="e19b2-121">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="e19b2-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e19b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19b2-122">CommonParameters</span></span>
<span data-ttu-id="e19b2-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19b2-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e19b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19b2-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e19b2-125">INPUTS</span></span>

### <span data-ttu-id="e19b2-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="e19b2-126">PSProfile</span></span>
<span data-ttu-id="e19b2-127">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e19b2-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="e19b2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e19b2-128">OUTPUTS</span></span>

###  
<span data-ttu-id="e19b2-129">Esse cmdlet retorna um objeto de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e19b2-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="e19b2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e19b2-130">NOTES</span></span>

## <span data-ttu-id="e19b2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e19b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="e19b2-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e19b2-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e19b2-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e19b2-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e19b2-136">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e19b2-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


