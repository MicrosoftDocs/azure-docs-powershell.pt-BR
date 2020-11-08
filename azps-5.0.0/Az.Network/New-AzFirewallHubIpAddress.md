---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118324"
---
# <span data-ttu-id="ca304-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca304-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="ca304-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca304-102">SYNOPSIS</span></span>
<span data-ttu-id="ca304-103">Endereços IP assoicated ao firewall no virtual Hub</span><span class="sxs-lookup"><span data-stu-id="ca304-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="ca304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca304-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca304-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca304-105">DESCRIPTION</span></span>
<span data-ttu-id="ca304-106">Endereços IP assoicated ao firewall no virtual Hub.</span><span class="sxs-lookup"><span data-stu-id="ca304-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="ca304-107">Podem ser endereços públicos e privados</span><span class="sxs-lookup"><span data-stu-id="ca304-107">These can be public and private addresses</span></span>

## <span data-ttu-id="ca304-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca304-108">EXAMPLES</span></span>

### <span data-ttu-id="ca304-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca304-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="ca304-110">Este exemplo cria um objeto de endereço IP de Hub com uma contagem de 2 IPs públicos.</span><span class="sxs-lookup"><span data-stu-id="ca304-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="ca304-111">O objeto HubIPAddress é ssociated para o firewall no Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="ca304-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="ca304-112">OS</span><span class="sxs-lookup"><span data-stu-id="ca304-112">PARAMETERS</span></span>

### <span data-ttu-id="ca304-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca304-113">-DefaultProfile</span></span>
<span data-ttu-id="ca304-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca304-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca304-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="ca304-115">-PrivateIPAddress</span></span>
<span data-ttu-id="ca304-116">O endereço IP privado do firewall anexado a um hub</span><span class="sxs-lookup"><span data-stu-id="ca304-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="ca304-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="ca304-117">-PublicIPs</span></span>
<span data-ttu-id="ca304-118">Os endereços IP do firewall anexado a um hub</span><span class="sxs-lookup"><span data-stu-id="ca304-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="ca304-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca304-119">-Confirm</span></span>
<span data-ttu-id="ca304-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca304-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca304-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca304-121">-WhatIf</span></span>
<span data-ttu-id="ca304-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca304-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca304-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca304-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca304-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca304-124">CommonParameters</span></span>
<span data-ttu-id="ca304-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca304-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca304-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca304-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca304-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca304-127">INPUTS</span></span>

### <span data-ttu-id="ca304-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ca304-128">None</span></span>

## <span data-ttu-id="ca304-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca304-129">OUTPUTS</span></span>

### <span data-ttu-id="ca304-130">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="ca304-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="ca304-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca304-131">NOTES</span></span>

## <span data-ttu-id="ca304-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca304-132">RELATED LINKS</span></span>
