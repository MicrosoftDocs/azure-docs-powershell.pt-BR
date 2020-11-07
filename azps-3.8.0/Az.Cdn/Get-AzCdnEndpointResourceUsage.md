---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942125"
---
# <span data-ttu-id="f049c-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f049c-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="f049c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f049c-102">SYNOPSIS</span></span>
<span data-ttu-id="f049c-103">Obtém o uso do recurso de um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="f049c-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="f049c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f049c-104">SYNTAX</span></span>

### <span data-ttu-id="f049c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f049c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f049c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f049c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f049c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f049c-107">DESCRIPTION</span></span>
<span data-ttu-id="f049c-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="f049c-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f049c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f049c-109">EXAMPLES</span></span>

### <span data-ttu-id="f049c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f049c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f049c-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="f049c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="f049c-112">OS</span><span class="sxs-lookup"><span data-stu-id="f049c-112">PARAMETERS</span></span>

### <span data-ttu-id="f049c-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f049c-113">-CdnEndpoint</span></span>
<span data-ttu-id="f049c-114">O objeto de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="f049c-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="f049c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f049c-115">-DefaultProfile</span></span>
<span data-ttu-id="f049c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f049c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f049c-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f049c-117">-EndpointName</span></span>
<span data-ttu-id="f049c-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="f049c-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f049c-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f049c-119">-ProfileName</span></span>
<span data-ttu-id="f049c-120">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="f049c-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f049c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f049c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f049c-122">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="f049c-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="f049c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f049c-123">CommonParameters</span></span>
<span data-ttu-id="f049c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f049c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f049c-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f049c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f049c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f049c-126">INPUTS</span></span>

### <span data-ttu-id="f049c-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f049c-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f049c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f049c-128">OUTPUTS</span></span>

### <span data-ttu-id="f049c-129">Microsoft. Azure. Commands. cdn. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="f049c-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="f049c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f049c-130">NOTES</span></span>

## <span data-ttu-id="f049c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f049c-131">RELATED LINKS</span></span>
