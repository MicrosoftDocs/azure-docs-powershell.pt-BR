---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118322"
---
# <span data-ttu-id="399f1-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="399f1-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="399f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="399f1-102">SYNOPSIS</span></span>
<span data-ttu-id="399f1-103">Ip público assoicado ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="399f1-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="399f1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="399f1-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="399f1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="399f1-105">DESCRIPTION</span></span>
<span data-ttu-id="399f1-106">Ip público assoicado ao firewall no hub virtual</span><span class="sxs-lookup"><span data-stu-id="399f1-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="399f1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="399f1-107">EXAMPLES</span></span>

### <span data-ttu-id="399f1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="399f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="399f1-109">Isso criará dois ips públicos no firewall anexado ao hub virtual.</span><span class="sxs-lookup"><span data-stu-id="399f1-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="399f1-110">Isso criará o endereço IP no back-end. Não é possível fornecer os endereços de ipad explicitamente para um novo firewall.</span><span class="sxs-lookup"><span data-stu-id="399f1-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="399f1-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="399f1-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="399f1-112">Isso criará 1 novo ip público no firewall mantendo $publicIp 1, $publicIp 2 que já existem no firewall.</span><span class="sxs-lookup"><span data-stu-id="399f1-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="399f1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="399f1-113">PARAMETERS</span></span>

### <span data-ttu-id="399f1-114">-Endereços</span><span class="sxs-lookup"><span data-stu-id="399f1-114">-Addresses</span></span>
<span data-ttu-id="399f1-115">Os Endereços IP Públicos do Firewall anexados a um hub</span><span class="sxs-lookup"><span data-stu-id="399f1-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="399f1-116">-Contagem</span><span class="sxs-lookup"><span data-stu-id="399f1-116">-Count</span></span>
<span data-ttu-id="399f1-117">A contagem de endereços Ip públicos</span><span class="sxs-lookup"><span data-stu-id="399f1-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="399f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="399f1-118">-DefaultProfile</span></span>
<span data-ttu-id="399f1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="399f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="399f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399f1-120">CommonParameters</span></span>
<span data-ttu-id="399f1-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="399f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399f1-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="399f1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399f1-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="399f1-123">INPUTS</span></span>

### <span data-ttu-id="399f1-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="399f1-124">None</span></span>

## <span data-ttu-id="399f1-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="399f1-125">OUTPUTS</span></span>

### <span data-ttu-id="399f1-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="399f1-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="399f1-127">Notas</span><span class="sxs-lookup"><span data-stu-id="399f1-127">NOTES</span></span>

## <span data-ttu-id="399f1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="399f1-128">RELATED LINKS</span></span>
