---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786406"
---
# <span data-ttu-id="14249-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14249-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="14249-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14249-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14249-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14249-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14249-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14249-104">DESCRIPTION</span></span>

## <span data-ttu-id="14249-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14249-105">EXAMPLES</span></span>

### <span data-ttu-id="14249-106">1:</span><span class="sxs-lookup"><span data-stu-id="14249-106">1:</span></span>
```

```

## <span data-ttu-id="14249-107">OS</span><span class="sxs-lookup"><span data-stu-id="14249-107">PARAMETERS</span></span>

### <span data-ttu-id="14249-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14249-108">-DefaultProfile</span></span>
<span data-ttu-id="14249-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14249-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14249-110">-Force</span><span class="sxs-lookup"><span data-stu-id="14249-110">-Force</span></span>
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

### <span data-ttu-id="14249-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="14249-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14249-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="14249-112">-Name</span></span>
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

### <span data-ttu-id="14249-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14249-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="14249-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14249-114">-Confirm</span></span>
<span data-ttu-id="14249-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14249-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14249-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14249-116">-WhatIf</span></span>
<span data-ttu-id="14249-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14249-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14249-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14249-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14249-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14249-119">CommonParameters</span></span>
<span data-ttu-id="14249-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14249-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14249-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14249-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14249-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14249-122">INPUTS</span></span>

## <span data-ttu-id="14249-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14249-123">OUTPUTS</span></span>

### <span data-ttu-id="14249-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14249-124">System.String</span></span>

## <span data-ttu-id="14249-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14249-125">NOTES</span></span>

## <span data-ttu-id="14249-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14249-126">RELATED LINKS</span></span>

[<span data-ttu-id="14249-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14249-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="14249-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="14249-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


