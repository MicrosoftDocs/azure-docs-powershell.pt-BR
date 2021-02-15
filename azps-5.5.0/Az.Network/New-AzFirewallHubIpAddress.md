---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114137"
---
# <span data-ttu-id="8dd5c-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="8dd5c-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="8dd5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd5c-103">Endereços ip associados ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="8dd5c-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="8dd5c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8dd5c-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd5c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8dd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd5c-106">Endereços IP associados ao firewall no hub virtual.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="8dd5c-107">Eles podem ser endereços públicos e privados</span><span class="sxs-lookup"><span data-stu-id="8dd5c-107">These can be public and private addresses</span></span>

## <span data-ttu-id="8dd5c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8dd5c-108">EXAMPLES</span></span>

### <span data-ttu-id="8dd5c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8dd5c-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="8dd5c-110">Este exemplo cria um objeto de endereço Ip do Hub com uma contagem de 2 IPs públicos.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="8dd5c-111">O objeto HubIPAddress éssociado ao firewall no hub virtual.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="8dd5c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dd5c-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd5c-113">-DefaultProfile</span></span>
<span data-ttu-id="8dd5c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd5c-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="8dd5c-115">-PrivateIPAddress</span></span>
<span data-ttu-id="8dd5c-116">O Endereço Ip particular do Firewall anexado a um Hub</span><span class="sxs-lookup"><span data-stu-id="8dd5c-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="8dd5c-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="8dd5c-117">-PublicIPs</span></span>
<span data-ttu-id="8dd5c-118">Os endereços IP do Firewall anexados a um hub</span><span class="sxs-lookup"><span data-stu-id="8dd5c-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="8dd5c-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8dd5c-119">-Confirm</span></span>
<span data-ttu-id="8dd5c-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd5c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd5c-121">-WhatIf</span></span>
<span data-ttu-id="8dd5c-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd5c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd5c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd5c-124">CommonParameters</span></span>
<span data-ttu-id="8dd5c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd5c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd5c-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dd5c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd5c-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="8dd5c-127">INPUTS</span></span>

### <span data-ttu-id="8dd5c-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8dd5c-128">None</span></span>

## <span data-ttu-id="8dd5c-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="8dd5c-129">OUTPUTS</span></span>

### <span data-ttu-id="8dd5c-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="8dd5c-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="8dd5c-131">Notas</span><span class="sxs-lookup"><span data-stu-id="8dd5c-131">NOTES</span></span>

## <span data-ttu-id="8dd5c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dd5c-132">RELATED LINKS</span></span>
