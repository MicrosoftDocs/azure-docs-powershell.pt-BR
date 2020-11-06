---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440841"
---
# <span data-ttu-id="abf84-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="abf84-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="abf84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abf84-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abf84-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abf84-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abf84-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abf84-104">DESCRIPTION</span></span>

## <span data-ttu-id="abf84-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abf84-105">EXAMPLES</span></span>

## <span data-ttu-id="abf84-106">OS</span><span class="sxs-lookup"><span data-stu-id="abf84-106">PARAMETERS</span></span>

### <span data-ttu-id="abf84-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf84-107">-DefaultProfile</span></span>
<span data-ttu-id="abf84-108">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abf84-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf84-109">-Force</span><span class="sxs-lookup"><span data-stu-id="abf84-109">-Force</span></span>
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

### <span data-ttu-id="abf84-110">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="abf84-110">-KeyLength</span></span>
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

### <span data-ttu-id="abf84-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="abf84-111">-Name</span></span>
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

### <span data-ttu-id="abf84-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf84-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="abf84-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abf84-113">-Confirm</span></span>
<span data-ttu-id="abf84-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abf84-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf84-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf84-115">-WhatIf</span></span>
<span data-ttu-id="abf84-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abf84-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf84-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abf84-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf84-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf84-118">CommonParameters</span></span>
<span data-ttu-id="abf84-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf84-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf84-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf84-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf84-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abf84-121">INPUTS</span></span>

### <span data-ttu-id="abf84-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="abf84-122">None</span></span>
<span data-ttu-id="abf84-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="abf84-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abf84-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abf84-124">OUTPUTS</span></span>

### <span data-ttu-id="abf84-125">System. String</span><span class="sxs-lookup"><span data-stu-id="abf84-125">System.String</span></span>

## <span data-ttu-id="abf84-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abf84-126">NOTES</span></span>

## <span data-ttu-id="abf84-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abf84-127">RELATED LINKS</span></span>

[<span data-ttu-id="abf84-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="abf84-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="abf84-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="abf84-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


