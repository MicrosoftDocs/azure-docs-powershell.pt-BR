---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: 43a92375126411d392623095a6753072757f49a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889638"
---
# <span data-ttu-id="81c28-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="81c28-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="81c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c28-102">SYNOPSIS</span></span>
<span data-ttu-id="81c28-103">Ip público assoicado ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="81c28-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="81c28-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81c28-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c28-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81c28-105">DESCRIPTION</span></span>
<span data-ttu-id="81c28-106">Ip público assoicado ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="81c28-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="81c28-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81c28-107">EXAMPLES</span></span>

### <span data-ttu-id="81c28-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81c28-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="81c28-109">Isso criará dois ips públicos no firewall anexado ao hub virtual.</span><span class="sxs-lookup"><span data-stu-id="81c28-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="81c28-110">Isso criará o endereço ip no back-end. Não podemos fornecer os ipaddresses explicitamente para um novo firewall.</span><span class="sxs-lookup"><span data-stu-id="81c28-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="81c28-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81c28-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="81c28-112">Isso criará um novo ip público no firewall mantendo $publicIp 1, $publicIp 2 que já existem no firewall.</span><span class="sxs-lookup"><span data-stu-id="81c28-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="81c28-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81c28-113">PARAMETERS</span></span>

### <span data-ttu-id="81c28-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="81c28-114">-Addresses</span></span>
<span data-ttu-id="81c28-115">Os endereços IP públicos do Firewall anexados a um hub</span><span class="sxs-lookup"><span data-stu-id="81c28-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c28-116">-Count</span><span class="sxs-lookup"><span data-stu-id="81c28-116">-Count</span></span>
<span data-ttu-id="81c28-117">A contagem de endereços Ip públicos</span><span class="sxs-lookup"><span data-stu-id="81c28-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c28-118">-DefaultProfile</span></span>
<span data-ttu-id="81c28-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81c28-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c28-120">CommonParameters</span></span>
<span data-ttu-id="81c28-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c28-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81c28-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c28-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81c28-123">INPUTS</span></span>

### <span data-ttu-id="81c28-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="81c28-124">None</span></span>

## <span data-ttu-id="81c28-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81c28-125">OUTPUTS</span></span>

### <span data-ttu-id="81c28-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="81c28-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="81c28-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="81c28-127">NOTES</span></span>

## <span data-ttu-id="81c28-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81c28-128">RELATED LINKS</span></span>
