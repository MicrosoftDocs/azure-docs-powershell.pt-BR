---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 14a77eeaeb502c79663f9d95cbff3ffc199ddc67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888237"
---
# <span data-ttu-id="2a308-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2a308-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="2a308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a308-102">SYNOPSIS</span></span>
<span data-ttu-id="2a308-103">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="2a308-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="2a308-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2a308-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a308-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2a308-105">DESCRIPTION</span></span>
<span data-ttu-id="2a308-106">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="2a308-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="2a308-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a308-107">EXAMPLES</span></span>

### <span data-ttu-id="2a308-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a308-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="2a308-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2a308-109">PARAMETERS</span></span>

### <span data-ttu-id="2a308-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a308-110">-DefaultProfile</span></span>
<span data-ttu-id="2a308-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2a308-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a308-112">-Name</span><span class="sxs-lookup"><span data-stu-id="2a308-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a308-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a308-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2a308-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a308-114">CommonParameters</span></span>
<span data-ttu-id="2a308-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a308-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a308-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a308-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a308-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a308-117">INPUTS</span></span>

### <span data-ttu-id="2a308-118">System.String</span><span class="sxs-lookup"><span data-stu-id="2a308-118">System.String</span></span>

## <span data-ttu-id="2a308-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2a308-119">OUTPUTS</span></span>

### <span data-ttu-id="2a308-120">System.String</span><span class="sxs-lookup"><span data-stu-id="2a308-120">System.String</span></span>

## <span data-ttu-id="2a308-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="2a308-121">NOTES</span></span>

## <span data-ttu-id="2a308-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a308-122">RELATED LINKS</span></span>

[<span data-ttu-id="2a308-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2a308-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="2a308-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2a308-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
