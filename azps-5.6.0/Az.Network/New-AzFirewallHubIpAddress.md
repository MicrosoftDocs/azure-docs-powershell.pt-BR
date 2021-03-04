---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: 333e245b77869903b74973a4f851d020d70c0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889640"
---
# <span data-ttu-id="bf8d7-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="bf8d7-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="bf8d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8d7-103">Endereços ip associados ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="bf8d7-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="bf8d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf8d7-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf8d7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf8d7-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8d7-106">Endereços ip associados ao firewall no hub virtual.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="bf8d7-107">Eles podem ser endereços públicos e privados</span><span class="sxs-lookup"><span data-stu-id="bf8d7-107">These can be public and private addresses</span></span>

## <span data-ttu-id="bf8d7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-108">EXAMPLES</span></span>

### <span data-ttu-id="bf8d7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf8d7-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="bf8d7-110">Este exemplo cria um objeto de endereço Ip do Hub com uma contagem de 2 IPs públicos.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="bf8d7-111">O objeto HubIPAddress éssociado ao firewall no hub virtual.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="bf8d7-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-112">PARAMETERS</span></span>

### <span data-ttu-id="bf8d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8d7-113">-DefaultProfile</span></span>
<span data-ttu-id="bf8d7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf8d7-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="bf8d7-115">-PrivateIPAddress</span></span>
<span data-ttu-id="bf8d7-116">O Endereço Ip privado do Firewall anexado a um Hub</span><span class="sxs-lookup"><span data-stu-id="bf8d7-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="bf8d7-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="bf8d7-117">-PublicIPs</span></span>
<span data-ttu-id="bf8d7-118">Os endereços IP do Firewall anexados a um hub</span><span class="sxs-lookup"><span data-stu-id="bf8d7-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8d7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf8d7-119">-Confirm</span></span>
<span data-ttu-id="bf8d7-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8d7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8d7-121">-WhatIf</span></span>
<span data-ttu-id="bf8d7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf8d7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf8d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8d7-124">CommonParameters</span></span>
<span data-ttu-id="bf8d7-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf8d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8d7-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf8d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8d7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-127">INPUTS</span></span>

### <span data-ttu-id="bf8d7-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bf8d7-128">None</span></span>

## <span data-ttu-id="bf8d7-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-129">OUTPUTS</span></span>

### <span data-ttu-id="bf8d7-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="bf8d7-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="bf8d7-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf8d7-131">NOTES</span></span>

## <span data-ttu-id="bf8d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf8d7-132">RELATED LINKS</span></span>
