---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2683af757bc1b0b58ebb6865a1cfd1edeef580e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776500"
---
# <span data-ttu-id="4ed5b-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ed5b-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="4ed5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ed5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed5b-103">Configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4ed5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ed5b-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed5b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ed5b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed5b-106">O cmdlet **set-AzVirtualNetworkGatewayConnectionSharedKey** configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4ed5b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ed5b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed5b-108">1:</span><span class="sxs-lookup"><span data-stu-id="4ed5b-108">1:</span></span>
```

```

## <span data-ttu-id="4ed5b-109">OS</span><span class="sxs-lookup"><span data-stu-id="4ed5b-109">PARAMETERS</span></span>

### <span data-ttu-id="4ed5b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed5b-110">-DefaultProfile</span></span>
<span data-ttu-id="4ed5b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4ed5b-112">-Force</span></span>
<span data-ttu-id="4ed5b-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ed5b-114">-Name</span></span>
<span data-ttu-id="4ed5b-115">Especifica o nome da chave compartilhada do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed5b-116">-ResourceGroupName</span></span>
<span data-ttu-id="4ed5b-117">Especifica o nome do grupo de recursos ao qual pertence o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4ed5b-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-118">-Valor</span><span class="sxs-lookup"><span data-stu-id="4ed5b-118">-Value</span></span>
<span data-ttu-id="4ed5b-119">Especifica o valor da chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-119">Specifies the value of the shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ed5b-120">-Confirm</span></span>
<span data-ttu-id="4ed5b-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed5b-122">-WhatIf</span></span>
<span data-ttu-id="4ed5b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed5b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed5b-125">CommonParameters</span></span>
<span data-ttu-id="4ed5b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed5b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed5b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed5b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ed5b-128">INPUTS</span></span>

## <span data-ttu-id="4ed5b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ed5b-129">OUTPUTS</span></span>

### <span data-ttu-id="4ed5b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4ed5b-130">System.String</span></span>

## <span data-ttu-id="4ed5b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ed5b-131">NOTES</span></span>

## <span data-ttu-id="4ed5b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ed5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="4ed5b-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ed5b-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="4ed5b-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4ed5b-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

