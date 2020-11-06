---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432663"
---
# <span data-ttu-id="361b5-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="361b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="361b5-102">SYNOPSIS</span></span>
<span data-ttu-id="361b5-103">Obtém um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="361b5-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="361b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="361b5-104">SYNTAX</span></span>

### <span data-ttu-id="361b5-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="361b5-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="361b5-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="361b5-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="361b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="361b5-107">DESCRIPTION</span></span>
<span data-ttu-id="361b5-108">O cmdlet **Get-AzureRMCdnEndpoint** Obtém um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="361b5-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="361b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="361b5-109">EXAMPLES</span></span>

## <span data-ttu-id="361b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="361b5-110">PARAMETERS</span></span>

### <span data-ttu-id="361b5-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="361b5-111">-CdnProfile</span></span>
<span data-ttu-id="361b5-112">Especifica o objeto de perfil CDN ao qual pertence o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="361b5-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="361b5-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="361b5-113">-EndpointName</span></span>
<span data-ttu-id="361b5-114">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="361b5-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="361b5-115">O nome do ponto de extremidade não é o nome de host do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="361b5-115">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="361b5-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="361b5-116">-ProfileName</span></span>
<span data-ttu-id="361b5-117">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="361b5-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="361b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="361b5-119">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="361b5-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="361b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361b5-120">-DefaultProfile</span></span>
<span data-ttu-id="361b5-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="361b5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="361b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361b5-122">CommonParameters</span></span>
<span data-ttu-id="361b5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361b5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="361b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361b5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="361b5-125">INPUTS</span></span>

### <span data-ttu-id="361b5-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="361b5-126">PSProfile</span></span>
<span data-ttu-id="361b5-127">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="361b5-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="361b5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="361b5-128">OUTPUTS</span></span>

###  
<span data-ttu-id="361b5-129">Esse cmdlet retorna um objeto de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="361b5-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="361b5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="361b5-130">NOTES</span></span>

## <span data-ttu-id="361b5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="361b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="361b5-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="361b5-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="361b5-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="361b5-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="361b5-136">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="361b5-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


