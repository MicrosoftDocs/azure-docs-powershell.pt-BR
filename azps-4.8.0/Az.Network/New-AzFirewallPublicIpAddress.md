---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111585"
---
# <span data-ttu-id="ae762-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae762-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="ae762-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae762-102">SYNOPSIS</span></span>
<span data-ttu-id="ae762-103">Este é o espaço reservado para o endereço IP que pode ser usado para vários Pip no firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae762-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="ae762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae762-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae762-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae762-105">DESCRIPTION</span></span>
<span data-ttu-id="ae762-106">Este é o espaço reservado para o endereço IP que pode ser usado para vários Pip no firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae762-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="ae762-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae762-107">EXAMPLES</span></span>

### <span data-ttu-id="ae762-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae762-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="ae762-109">$publicIp será o espaço reservado para o endereço de IP 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="ae762-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="ae762-110">OS</span><span class="sxs-lookup"><span data-stu-id="ae762-110">PARAMETERS</span></span>

### <span data-ttu-id="ae762-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="ae762-111">-Address</span></span>
<span data-ttu-id="ae762-112">Os endereços IP do firewall anexado a um hub</span><span class="sxs-lookup"><span data-stu-id="ae762-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="ae762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae762-113">-DefaultProfile</span></span>
<span data-ttu-id="ae762-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae762-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae762-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae762-115">-Confirm</span></span>
<span data-ttu-id="ae762-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae762-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae762-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae762-117">-WhatIf</span></span>
<span data-ttu-id="ae762-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae762-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae762-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae762-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae762-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae762-120">CommonParameters</span></span>
<span data-ttu-id="ae762-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae762-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae762-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae762-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae762-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae762-123">INPUTS</span></span>

### <span data-ttu-id="ae762-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ae762-124">None</span></span>

## <span data-ttu-id="ae762-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae762-125">OUTPUTS</span></span>

### <span data-ttu-id="ae762-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ae762-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="ae762-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae762-127">NOTES</span></span>

## <span data-ttu-id="ae762-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae762-128">RELATED LINKS</span></span>
