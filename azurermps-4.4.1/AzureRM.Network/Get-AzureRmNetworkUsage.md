---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkUsage.md
ms.openlocfilehash: c5bb92ad330b49ff015f21ae14fab42d6583305c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441007"
---
# <span data-ttu-id="40d7e-101">Get-AzureRmNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="40d7e-101">Get-AzureRmNetworkUsage</span></span>

## <span data-ttu-id="40d7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="40d7e-103">Lista os usos da rede para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="40d7e-103">Lists network usages for a subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40d7e-104">SYNTAX</span></span>

```
Get-AzureRmNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d7e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="40d7e-106">O cmdlet Get-AzureRmNetworkUsage Obtém limites e uso atual para recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="40d7e-106">The Get-AzureRmNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="40d7e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="40d7e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40d7e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmNetworkUsage -Location westcentralus

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

<span data-ttu-id="40d7e-109">Obtém dados de uso de recursos na região westcentralus</span><span class="sxs-lookup"><span data-stu-id="40d7e-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="40d7e-110">OS</span><span class="sxs-lookup"><span data-stu-id="40d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="40d7e-111">-Local</span><span class="sxs-lookup"><span data-stu-id="40d7e-111">-Location</span></span>
<span data-ttu-id="40d7e-112">O local em que o uso do recurso é consultado.</span><span class="sxs-lookup"><span data-stu-id="40d7e-112">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="40d7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d7e-113">-DefaultProfile</span></span>
<span data-ttu-id="40d7e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40d7e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d7e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d7e-115">CommonParameters</span></span>
<span data-ttu-id="40d7e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d7e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d7e-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d7e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d7e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40d7e-118">INPUTS</span></span>

### <span data-ttu-id="40d7e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="40d7e-119">System.String</span></span>

## <span data-ttu-id="40d7e-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40d7e-120">OUTPUTS</span></span>

### <span data-ttu-id="40d7e-121">Microsoft. Azure. Commands. Network. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="40d7e-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="40d7e-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40d7e-122">NOTES</span></span>

## <span data-ttu-id="40d7e-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40d7e-123">RELATED LINKS</span></span>

