---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117914"
---
# <span data-ttu-id="d4bea-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d4bea-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="d4bea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4bea-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bea-103">Obtém o uso do recurso de um ponto de extremidade de CDN.</span><span class="sxs-lookup"><span data-stu-id="d4bea-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="d4bea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4bea-104">SYNTAX</span></span>

### <span data-ttu-id="d4bea-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4bea-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4bea-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4bea-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4bea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4bea-107">DESCRIPTION</span></span>
<span data-ttu-id="d4bea-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="d4bea-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d4bea-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4bea-109">EXAMPLES</span></span>

### <span data-ttu-id="d4bea-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4bea-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d4bea-111">{{ Adicione a descrição do exemplo aqui }}</span><span class="sxs-lookup"><span data-stu-id="d4bea-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d4bea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4bea-112">PARAMETERS</span></span>

### <span data-ttu-id="d4bea-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bea-113">-CdnEndpoint</span></span>
<span data-ttu-id="d4bea-114">O objeto de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="d4bea-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="d4bea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bea-115">-DefaultProfile</span></span>
<span data-ttu-id="d4bea-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d4bea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4bea-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="d4bea-117">-EndpointName</span></span>
<span data-ttu-id="d4bea-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bea-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d4bea-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d4bea-119">-ProfileName</span></span>
<span data-ttu-id="d4bea-120">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bea-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d4bea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4bea-121">-ResourceGroupName</span></span>
<span data-ttu-id="d4bea-122">O grupo de recursos do Perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bea-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="d4bea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bea-123">CommonParameters</span></span>
<span data-ttu-id="d4bea-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4bea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bea-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4bea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bea-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="d4bea-126">INPUTS</span></span>

### <span data-ttu-id="d4bea-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4bea-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d4bea-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="d4bea-128">OUTPUTS</span></span>

### <span data-ttu-id="d4bea-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d4bea-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="d4bea-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d4bea-130">NOTES</span></span>

## <span data-ttu-id="d4bea-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4bea-131">RELATED LINKS</span></span>
