---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602171"
---
# <span data-ttu-id="e711c-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e711c-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="e711c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e711c-102">SYNOPSIS</span></span>
<span data-ttu-id="e711c-103">Obtém um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="e711c-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e711c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e711c-104">SYNTAX</span></span>

### <span data-ttu-id="e711c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e711c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e711c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e711c-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e711c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e711c-107">DESCRIPTION</span></span>
<span data-ttu-id="e711c-108">O cmdlet **Get-AzureRmCdnOrigin** Obtém um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure e seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="e711c-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="e711c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e711c-109">EXAMPLES</span></span>

## <span data-ttu-id="e711c-110">OS</span><span class="sxs-lookup"><span data-stu-id="e711c-110">PARAMETERS</span></span>

### <span data-ttu-id="e711c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e711c-111">-CdnEndpoint</span></span>
<span data-ttu-id="e711c-112">Especifica o objeto de ponto de extremidade CDN ao qual a origem pertence.</span><span class="sxs-lookup"><span data-stu-id="e711c-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="e711c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e711c-113">-DefaultProfile</span></span>
<span data-ttu-id="e711c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e711c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e711c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e711c-115">-EndpointName</span></span>
<span data-ttu-id="e711c-116">Especifica o nome do ponto de extremidade ao qual pertence o servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="e711c-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e711c-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="e711c-117">-OriginName</span></span>
<span data-ttu-id="e711c-118">Especifica o nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="e711c-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="e711c-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e711c-119">-ProfileName</span></span>
<span data-ttu-id="e711c-120">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="e711c-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e711c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e711c-121">-ResourceGroupName</span></span>
<span data-ttu-id="e711c-122">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="e711c-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e711c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e711c-123">CommonParameters</span></span>
<span data-ttu-id="e711c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e711c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e711c-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e711c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e711c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e711c-126">INPUTS</span></span>

### <span data-ttu-id="e711c-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e711c-127">PSEndpoint</span></span>
<span data-ttu-id="e711c-128">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e711c-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e711c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e711c-129">OUTPUTS</span></span>

###  
<span data-ttu-id="e711c-130">Esse cmdlet retorna um objeto de servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="e711c-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="e711c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e711c-131">NOTES</span></span>

## <span data-ttu-id="e711c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e711c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e711c-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e711c-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


