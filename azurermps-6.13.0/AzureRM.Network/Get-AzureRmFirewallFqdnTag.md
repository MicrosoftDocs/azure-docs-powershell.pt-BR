---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610560"
---
# <span data-ttu-id="01833-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="01833-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="01833-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01833-102">SYNOPSIS</span></span>
<span data-ttu-id="01833-103">Obtém as marcas de FQDN do firewall do Azure disponíveis.</span><span class="sxs-lookup"><span data-stu-id="01833-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01833-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01833-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01833-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01833-105">DESCRIPTION</span></span>
<span data-ttu-id="01833-106">O cmdlet **Get-AzureRmFirewallFqdnTag** Obtém a lista de marcas de FQDN que podem ser usadas para as regras do aplicativo de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="01833-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="01833-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01833-107">EXAMPLES</span></span>

### <span data-ttu-id="01833-108">1: recuperar todas as marcas de FQDN disponíveis</span><span class="sxs-lookup"><span data-stu-id="01833-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="01833-109">Este exemplo recupera todas as marcas FQDN disponíveis.</span><span class="sxs-lookup"><span data-stu-id="01833-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="01833-110">2: usar primeira marca FQDN disponível em uma regra de aplicativo</span><span class="sxs-lookup"><span data-stu-id="01833-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="01833-111">Este exemplo cria uma regra de aplicativo de firewall usando a primeira marca FQDN disponível</span><span class="sxs-lookup"><span data-stu-id="01833-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="01833-112">OS</span><span class="sxs-lookup"><span data-stu-id="01833-112">PARAMETERS</span></span>

### <span data-ttu-id="01833-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01833-113">-DefaultProfile</span></span>
<span data-ttu-id="01833-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01833-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01833-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01833-115">CommonParameters</span></span>
<span data-ttu-id="01833-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01833-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01833-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01833-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01833-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01833-118">INPUTS</span></span>

### <span data-ttu-id="01833-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="01833-119">None</span></span>
<span data-ttu-id="01833-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="01833-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01833-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01833-121">OUTPUTS</span></span>

### <span data-ttu-id="01833-122">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="01833-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="01833-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01833-123">NOTES</span></span>

## <span data-ttu-id="01833-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01833-124">RELATED LINKS</span></span>

[<span data-ttu-id="01833-125">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="01833-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="01833-126">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="01833-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
