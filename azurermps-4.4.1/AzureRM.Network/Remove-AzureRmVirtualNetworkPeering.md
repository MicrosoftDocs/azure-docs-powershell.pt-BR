---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610996"
---
# <span data-ttu-id="20abd-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20abd-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="20abd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20abd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20abd-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20abd-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20abd-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20abd-104">DESCRIPTION</span></span>

## <span data-ttu-id="20abd-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20abd-105">EXAMPLES</span></span>

### <span data-ttu-id="20abd-106">Exemplo 1: remover um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="20abd-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="20abd-107">OS</span><span class="sxs-lookup"><span data-stu-id="20abd-107">PARAMETERS</span></span>

### <span data-ttu-id="20abd-108">-Force</span><span class="sxs-lookup"><span data-stu-id="20abd-108">-Force</span></span>
<span data-ttu-id="20abd-109">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="20abd-109">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20abd-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="20abd-110">-Name</span></span>
<span data-ttu-id="20abd-111">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20abd-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="20abd-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20abd-112">-PassThru</span></span>
<span data-ttu-id="20abd-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="20abd-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20abd-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="20abd-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20abd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20abd-115">-ResourceGroupName</span></span>
<span data-ttu-id="20abd-116">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20abd-116">The resource group name</span></span>

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

### <span data-ttu-id="20abd-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="20abd-117">-VirtualNetworkName</span></span>
<span data-ttu-id="20abd-118">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20abd-118">The virtual network name.</span></span>

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

### <span data-ttu-id="20abd-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20abd-119">-Confirm</span></span>
<span data-ttu-id="20abd-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20abd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20abd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20abd-121">-WhatIf</span></span>
<span data-ttu-id="20abd-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20abd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20abd-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20abd-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20abd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20abd-124">-DefaultProfile</span></span>
<span data-ttu-id="20abd-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20abd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20abd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20abd-126">CommonParameters</span></span>
<span data-ttu-id="20abd-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20abd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20abd-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20abd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20abd-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20abd-129">INPUTS</span></span>

## <span data-ttu-id="20abd-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20abd-130">OUTPUTS</span></span>

## <span data-ttu-id="20abd-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20abd-131">NOTES</span></span>

## <span data-ttu-id="20abd-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20abd-132">RELATED LINKS</span></span>

