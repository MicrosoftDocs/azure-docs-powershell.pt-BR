---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: 0912ba8913bae430c3878dc0bde578420a5ea429
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427280"
---
# <span data-ttu-id="787a4-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="787a4-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="787a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="787a4-102">SYNOPSIS</span></span>
<span data-ttu-id="787a4-103">Obtém um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="787a4-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="787a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="787a4-104">SYNTAX</span></span>

### <span data-ttu-id="787a4-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="787a4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="787a4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="787a4-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="787a4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="787a4-107">DESCRIPTION</span></span>
<span data-ttu-id="787a4-108">O cmdlet **Get-AzureRmCdnOrigin** Obtém um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="787a4-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="787a4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="787a4-109">EXAMPLES</span></span>

## <span data-ttu-id="787a4-110">OS</span><span class="sxs-lookup"><span data-stu-id="787a4-110">PARAMETERS</span></span>

### <span data-ttu-id="787a4-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="787a4-111">-CdnEndpoint</span></span>
<span data-ttu-id="787a4-112">Especifica o objeto de ponto de extremidade CDN ao qual a origem pertence.</span><span class="sxs-lookup"><span data-stu-id="787a4-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="787a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787a4-113">-DefaultProfile</span></span>
<span data-ttu-id="787a4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="787a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="787a4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="787a4-115">-EndpointName</span></span>
<span data-ttu-id="787a4-116">Especifica o nome do ponto de extremidade ao qual pertence o servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="787a4-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="787a4-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="787a4-117">-OriginName</span></span>
<span data-ttu-id="787a4-118">Especifica o nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="787a4-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="787a4-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="787a4-119">-ProfileName</span></span>
<span data-ttu-id="787a4-120">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="787a4-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="787a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="787a4-122">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="787a4-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="787a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787a4-123">CommonParameters</span></span>
<span data-ttu-id="787a4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787a4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787a4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="787a4-126">INPUTS</span></span>

### <span data-ttu-id="787a4-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="787a4-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="787a4-128">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="787a4-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="787a4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="787a4-129">OUTPUTS</span></span>

### <span data-ttu-id="787a4-130">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="787a4-130">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="787a4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="787a4-131">NOTES</span></span>

## <span data-ttu-id="787a4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="787a4-132">RELATED LINKS</span></span>

[<span data-ttu-id="787a4-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="787a4-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


