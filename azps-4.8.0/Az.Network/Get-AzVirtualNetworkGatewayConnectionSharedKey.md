---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111028"
---
# <span data-ttu-id="f43ce-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f43ce-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f43ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f43ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f43ce-103">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="f43ce-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="f43ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f43ce-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f43ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f43ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f43ce-106">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="f43ce-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="f43ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f43ce-107">EXAMPLES</span></span>

### <span data-ttu-id="f43ce-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f43ce-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="f43ce-109">OS</span><span class="sxs-lookup"><span data-stu-id="f43ce-109">PARAMETERS</span></span>

### <span data-ttu-id="f43ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43ce-110">-DefaultProfile</span></span>
<span data-ttu-id="f43ce-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f43ce-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f43ce-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f43ce-112">-Name</span></span>
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

### <span data-ttu-id="f43ce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f43ce-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f43ce-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43ce-114">CommonParameters</span></span>
<span data-ttu-id="f43ce-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f43ce-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43ce-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f43ce-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43ce-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f43ce-117">INPUTS</span></span>

### <span data-ttu-id="f43ce-118">System. String</span><span class="sxs-lookup"><span data-stu-id="f43ce-118">System.String</span></span>

## <span data-ttu-id="f43ce-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f43ce-119">OUTPUTS</span></span>

### <span data-ttu-id="f43ce-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f43ce-120">System.String</span></span>

## <span data-ttu-id="f43ce-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f43ce-121">NOTES</span></span>

## <span data-ttu-id="f43ce-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f43ce-122">RELATED LINKS</span></span>

[<span data-ttu-id="f43ce-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f43ce-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f43ce-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f43ce-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
