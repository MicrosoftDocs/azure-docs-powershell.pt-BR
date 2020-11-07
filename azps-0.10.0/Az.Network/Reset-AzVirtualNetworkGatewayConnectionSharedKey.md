---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776589"
---
# <span data-ttu-id="7ffde-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ffde-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="7ffde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ffde-102">SYNOPSIS</span></span>

## <span data-ttu-id="7ffde-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ffde-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ffde-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ffde-104">DESCRIPTION</span></span>

## <span data-ttu-id="7ffde-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ffde-105">EXAMPLES</span></span>

### <span data-ttu-id="7ffde-106">1:</span><span class="sxs-lookup"><span data-stu-id="7ffde-106">1:</span></span>
```

```

## <span data-ttu-id="7ffde-107">OS</span><span class="sxs-lookup"><span data-stu-id="7ffde-107">PARAMETERS</span></span>

### <span data-ttu-id="7ffde-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffde-108">-DefaultProfile</span></span>
<span data-ttu-id="7ffde-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffde-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ffde-110">-Force</span><span class="sxs-lookup"><span data-stu-id="7ffde-110">-Force</span></span>
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

### <span data-ttu-id="7ffde-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="7ffde-111">-KeyLength</span></span>
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

### <span data-ttu-id="7ffde-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ffde-112">-Name</span></span>
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

### <span data-ttu-id="7ffde-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffde-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7ffde-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ffde-114">-Confirm</span></span>
<span data-ttu-id="7ffde-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ffde-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ffde-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffde-116">-WhatIf</span></span>
<span data-ttu-id="7ffde-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ffde-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffde-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ffde-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ffde-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffde-119">CommonParameters</span></span>
<span data-ttu-id="7ffde-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ffde-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffde-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffde-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffde-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ffde-122">INPUTS</span></span>

## <span data-ttu-id="7ffde-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ffde-123">OUTPUTS</span></span>

### <span data-ttu-id="7ffde-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7ffde-124">System.String</span></span>

## <span data-ttu-id="7ffde-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ffde-125">NOTES</span></span>

## <span data-ttu-id="7ffde-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ffde-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ffde-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ffde-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="7ffde-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ffde-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


