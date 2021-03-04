---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: 2e7c1b0468ed3faf37c8f11bc0cb1eca707195bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886204"
---
# <span data-ttu-id="78b02-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="78b02-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="78b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b02-102">SYNOPSIS</span></span>
<span data-ttu-id="78b02-103">Esse é o espaço reservado para o Endereço Ip que pode ser usado para vários pips no firewall do azure.</span><span class="sxs-lookup"><span data-stu-id="78b02-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="78b02-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78b02-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78b02-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78b02-105">DESCRIPTION</span></span>
<span data-ttu-id="78b02-106">Esse é o espaço reservado para o Endereço Ip que pode ser usado para vários pips no firewall do azure.</span><span class="sxs-lookup"><span data-stu-id="78b02-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="78b02-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78b02-107">EXAMPLES</span></span>

### <span data-ttu-id="78b02-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78b02-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="78b02-109">$publicIp será o espaço reservado para o endereço ip 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="78b02-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="78b02-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78b02-110">PARAMETERS</span></span>

### <span data-ttu-id="78b02-111">-Address</span><span class="sxs-lookup"><span data-stu-id="78b02-111">-Address</span></span>
<span data-ttu-id="78b02-112">Os endereços IP do Firewall anexados a um hub</span><span class="sxs-lookup"><span data-stu-id="78b02-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="78b02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b02-113">-DefaultProfile</span></span>
<span data-ttu-id="78b02-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78b02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b02-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78b02-115">-Confirm</span></span>
<span data-ttu-id="78b02-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78b02-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b02-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b02-117">-WhatIf</span></span>
<span data-ttu-id="78b02-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78b02-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78b02-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78b02-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b02-120">CommonParameters</span></span>
<span data-ttu-id="78b02-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b02-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78b02-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b02-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78b02-123">INPUTS</span></span>

### <span data-ttu-id="78b02-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="78b02-124">None</span></span>

## <span data-ttu-id="78b02-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78b02-125">OUTPUTS</span></span>

### <span data-ttu-id="78b02-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="78b02-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="78b02-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="78b02-127">NOTES</span></span>

## <span data-ttu-id="78b02-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78b02-128">RELATED LINKS</span></span>
