---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 071843c47ea3a8f97125746aa80fdb90eb1cb566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771965"
---
# <span data-ttu-id="83e94-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="83e94-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="83e94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83e94-102">SYNOPSIS</span></span>
<span data-ttu-id="83e94-103">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="83e94-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="83e94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83e94-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83e94-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83e94-105">DESCRIPTION</span></span>
<span data-ttu-id="83e94-106">Exibe a chave compartilhada usada para a conexão.</span><span class="sxs-lookup"><span data-stu-id="83e94-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="83e94-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83e94-107">EXAMPLES</span></span>

### <span data-ttu-id="83e94-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83e94-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="83e94-109">OS</span><span class="sxs-lookup"><span data-stu-id="83e94-109">PARAMETERS</span></span>

### <span data-ttu-id="83e94-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e94-110">-DefaultProfile</span></span>
<span data-ttu-id="83e94-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83e94-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e94-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="83e94-112">-Name</span></span>
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

### <span data-ttu-id="83e94-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e94-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="83e94-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e94-114">CommonParameters</span></span>
<span data-ttu-id="83e94-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e94-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e94-116">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83e94-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e94-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83e94-117">INPUTS</span></span>

### <span data-ttu-id="83e94-118">System. String</span><span class="sxs-lookup"><span data-stu-id="83e94-118">System.String</span></span>

## <span data-ttu-id="83e94-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83e94-119">OUTPUTS</span></span>

### <span data-ttu-id="83e94-120">System. String</span><span class="sxs-lookup"><span data-stu-id="83e94-120">System.String</span></span>

## <span data-ttu-id="83e94-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83e94-121">NOTES</span></span>

## <span data-ttu-id="83e94-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83e94-122">RELATED LINKS</span></span>

[<span data-ttu-id="83e94-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="83e94-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="83e94-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="83e94-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
