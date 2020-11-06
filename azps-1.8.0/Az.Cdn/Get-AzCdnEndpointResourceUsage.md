---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 1c9e83e8181d716024ae993ba0c3f5a9f75c6ef1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601420"
---
# <span data-ttu-id="4b4ca-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="4b4ca-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="4b4ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4ca-103">Obtém o uso do recurso de um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="4b4ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b4ca-104">SYNTAX</span></span>

### <span data-ttu-id="4b4ca-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b4ca-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4ca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b4ca-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4ca-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b4ca-107">DESCRIPTION</span></span>
<span data-ttu-id="4b4ca-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="4b4ca-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4b4ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b4ca-109">EXAMPLES</span></span>

### <span data-ttu-id="4b4ca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b4ca-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4b4ca-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="4b4ca-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4b4ca-112">OS</span><span class="sxs-lookup"><span data-stu-id="4b4ca-112">PARAMETERS</span></span>

### <span data-ttu-id="4b4ca-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4ca-113">-CdnEndpoint</span></span>
<span data-ttu-id="4b4ca-114">O objeto de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="4b4ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4ca-115">-DefaultProfile</span></span>
<span data-ttu-id="4b4ca-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4b4ca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b4ca-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4b4ca-117">-EndpointName</span></span>
<span data-ttu-id="4b4ca-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="4b4ca-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4b4ca-119">-ProfileName</span></span>
<span data-ttu-id="4b4ca-120">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="4b4ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b4ca-122">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="4b4ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4ca-123">CommonParameters</span></span>
<span data-ttu-id="4b4ca-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4ca-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4ca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4ca-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b4ca-126">INPUTS</span></span>

### <span data-ttu-id="4b4ca-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b4ca-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4b4ca-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b4ca-128">OUTPUTS</span></span>

### <span data-ttu-id="4b4ca-129">Microsoft. Azure. Commands. cdn. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="4b4ca-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="4b4ca-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b4ca-130">NOTES</span></span>

## <span data-ttu-id="4b4ca-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b4ca-131">RELATED LINKS</span></span>
