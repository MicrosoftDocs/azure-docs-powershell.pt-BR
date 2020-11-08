---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118322"
---
# <span data-ttu-id="44748-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="44748-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="44748-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44748-102">SYNOPSIS</span></span>
<span data-ttu-id="44748-103">Assoicated de IP público para o firewall no virtual Hub</span><span class="sxs-lookup"><span data-stu-id="44748-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="44748-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44748-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44748-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44748-105">DESCRIPTION</span></span>
<span data-ttu-id="44748-106">Assoicated de IP público para o firewall no virtual Hub</span><span class="sxs-lookup"><span data-stu-id="44748-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="44748-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44748-107">EXAMPLES</span></span>

### <span data-ttu-id="44748-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44748-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="44748-109">Isso criará dois IPS públicos no firewall anexado ao Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="44748-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="44748-110">Isso criará o endereço IP no back-end. Não podemos fornecer IPAddresses explicitamente para um novo firewall.</span><span class="sxs-lookup"><span data-stu-id="44748-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="44748-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44748-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="44748-112">Isso criará um 1 novo IP público no firewall, mantendo $publicIp 1 $publicIp 2 que já existem no firewall.</span><span class="sxs-lookup"><span data-stu-id="44748-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="44748-113">OS</span><span class="sxs-lookup"><span data-stu-id="44748-113">PARAMETERS</span></span>

### <span data-ttu-id="44748-114">-Endereços</span><span class="sxs-lookup"><span data-stu-id="44748-114">-Addresses</span></span>
<span data-ttu-id="44748-115">Os endereços IP públicos do firewall anexado a um hub</span><span class="sxs-lookup"><span data-stu-id="44748-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="44748-116">-Contagem</span><span class="sxs-lookup"><span data-stu-id="44748-116">-Count</span></span>
<span data-ttu-id="44748-117">A contagem de endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="44748-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="44748-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44748-118">-DefaultProfile</span></span>
<span data-ttu-id="44748-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44748-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44748-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44748-120">CommonParameters</span></span>
<span data-ttu-id="44748-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44748-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44748-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44748-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44748-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44748-123">INPUTS</span></span>

### <span data-ttu-id="44748-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44748-124">None</span></span>

## <span data-ttu-id="44748-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44748-125">OUTPUTS</span></span>

### <span data-ttu-id="44748-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="44748-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="44748-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44748-127">NOTES</span></span>

## <span data-ttu-id="44748-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44748-128">RELATED LINKS</span></span>
