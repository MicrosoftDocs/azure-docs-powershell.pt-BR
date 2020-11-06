---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428870"
---
# <span data-ttu-id="62cb5-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="62cb5-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="62cb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="62cb5-103">Configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="62cb5-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62cb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62cb5-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62cb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="62cb5-106">O cmdlet **set-AzureRmVirtualNetworkGatewayConnectionSharedKey** configura a chave compartilhada da conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="62cb5-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="62cb5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62cb5-107">EXAMPLES</span></span>

## <span data-ttu-id="62cb5-108">OS</span><span class="sxs-lookup"><span data-stu-id="62cb5-108">PARAMETERS</span></span>

### <span data-ttu-id="62cb5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62cb5-109">-DefaultProfile</span></span>
<span data-ttu-id="62cb5-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62cb5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62cb5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="62cb5-111">-Force</span></span>
<span data-ttu-id="62cb5-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="62cb5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62cb5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="62cb5-113">-Name</span></span>
<span data-ttu-id="62cb5-114">Especifica o nome da chave compartilhada do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="62cb5-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="62cb5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62cb5-115">-ResourceGroupName</span></span>
<span data-ttu-id="62cb5-116">Especifica o nome do grupo de recursos ao qual pertence o gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="62cb5-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="62cb5-117">-Valor</span><span class="sxs-lookup"><span data-stu-id="62cb5-117">-Value</span></span>
<span data-ttu-id="62cb5-118">Especifica o valor da chave compartilhada.</span><span class="sxs-lookup"><span data-stu-id="62cb5-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="62cb5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62cb5-119">-Confirm</span></span>
<span data-ttu-id="62cb5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62cb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62cb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62cb5-121">-WhatIf</span></span>
<span data-ttu-id="62cb5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62cb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62cb5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62cb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62cb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62cb5-124">CommonParameters</span></span>
<span data-ttu-id="62cb5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62cb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62cb5-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62cb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62cb5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62cb5-127">INPUTS</span></span>

### <span data-ttu-id="62cb5-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="62cb5-128">None</span></span>
<span data-ttu-id="62cb5-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="62cb5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62cb5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62cb5-130">OUTPUTS</span></span>

### <span data-ttu-id="62cb5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="62cb5-131">System.String</span></span>

## <span data-ttu-id="62cb5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62cb5-132">NOTES</span></span>

## <span data-ttu-id="62cb5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62cb5-133">RELATED LINKS</span></span>

[<span data-ttu-id="62cb5-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="62cb5-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="62cb5-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="62cb5-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


