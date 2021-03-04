---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901502"
---
# <span data-ttu-id="0f565-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="0f565-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="0f565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f565-102">SYNOPSIS</span></span>
<span data-ttu-id="0f565-103">Obtém o uso de recursos de um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="0f565-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="0f565-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f565-104">SYNTAX</span></span>

### <span data-ttu-id="0f565-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f565-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f565-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f565-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f565-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f565-107">DESCRIPTION</span></span>
<span data-ttu-id="0f565-108">{{Preencha a Descrição}}</span><span class="sxs-lookup"><span data-stu-id="0f565-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0f565-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f565-109">EXAMPLES</span></span>

### <span data-ttu-id="0f565-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f565-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0f565-111">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="0f565-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="0f565-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f565-112">PARAMETERS</span></span>

### <span data-ttu-id="0f565-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f565-113">-CdnEndpoint</span></span>
<span data-ttu-id="0f565-114">O objeto de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="0f565-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="0f565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f565-115">-DefaultProfile</span></span>
<span data-ttu-id="0f565-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0f565-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f565-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0f565-117">-EndpointName</span></span>
<span data-ttu-id="0f565-118">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f565-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0f565-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0f565-119">-ProfileName</span></span>
<span data-ttu-id="0f565-120">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f565-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0f565-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f565-121">-ResourceGroupName</span></span>
<span data-ttu-id="0f565-122">O grupo de recursos do Perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f565-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="0f565-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f565-123">CommonParameters</span></span>
<span data-ttu-id="0f565-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f565-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f565-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f565-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f565-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f565-126">INPUTS</span></span>

### <span data-ttu-id="0f565-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f565-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0f565-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f565-128">OUTPUTS</span></span>

### <span data-ttu-id="0f565-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="0f565-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="0f565-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f565-130">NOTES</span></span>

## <span data-ttu-id="0f565-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f565-131">RELATED LINKS</span></span>
