---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115170"
---
# <span data-ttu-id="1667a-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="1667a-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="1667a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1667a-102">SYNOPSIS</span></span>
<span data-ttu-id="1667a-103">Lista os usos de rede para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="1667a-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="1667a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1667a-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1667a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1667a-105">DESCRIPTION</span></span>
<span data-ttu-id="1667a-106">O Get-AzNetworkUsage cmdlet obtém limites e o uso atual dos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="1667a-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="1667a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1667a-107">EXAMPLES</span></span>

### <span data-ttu-id="1667a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1667a-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="1667a-109">Obtém dados de uso de recursos na região oeste</span><span class="sxs-lookup"><span data-stu-id="1667a-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="1667a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1667a-110">PARAMETERS</span></span>

### <span data-ttu-id="1667a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1667a-111">-DefaultProfile</span></span>
<span data-ttu-id="1667a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1667a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1667a-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1667a-113">-Location</span></span>
<span data-ttu-id="1667a-114">O local onde o uso do recurso é consultado.</span><span class="sxs-lookup"><span data-stu-id="1667a-114">The location where resource usage is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1667a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1667a-115">CommonParameters</span></span>
<span data-ttu-id="1667a-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1667a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1667a-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1667a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1667a-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="1667a-118">INPUTS</span></span>

### <span data-ttu-id="1667a-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1667a-119">System.String</span></span>

## <span data-ttu-id="1667a-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="1667a-120">OUTPUTS</span></span>

### <span data-ttu-id="1667a-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="1667a-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="1667a-122">Notas</span><span class="sxs-lookup"><span data-stu-id="1667a-122">NOTES</span></span>

## <span data-ttu-id="1667a-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1667a-123">RELATED LINKS</span></span>
