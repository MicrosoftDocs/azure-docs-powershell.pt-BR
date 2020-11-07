---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776593"
---
# <span data-ttu-id="09120-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="09120-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="09120-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09120-102">SYNOPSIS</span></span>

## <span data-ttu-id="09120-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09120-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09120-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09120-104">DESCRIPTION</span></span>

## <span data-ttu-id="09120-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09120-105">EXAMPLES</span></span>

### <span data-ttu-id="09120-106">Exemplo 1: remover um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="09120-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="09120-107">OS</span><span class="sxs-lookup"><span data-stu-id="09120-107">PARAMETERS</span></span>

### <span data-ttu-id="09120-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09120-108">-AsJob</span></span>
<span data-ttu-id="09120-109">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="09120-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09120-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09120-110">-DefaultProfile</span></span>
<span data-ttu-id="09120-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09120-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09120-112">-Force</span><span class="sxs-lookup"><span data-stu-id="09120-112">-Force</span></span>
<span data-ttu-id="09120-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="09120-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09120-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="09120-114">-Name</span></span>
<span data-ttu-id="09120-115">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09120-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="09120-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09120-116">-PassThru</span></span>
<span data-ttu-id="09120-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="09120-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="09120-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="09120-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="09120-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09120-119">-ResourceGroupName</span></span>
<span data-ttu-id="09120-120">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="09120-120">The resource group name</span></span>

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

### <span data-ttu-id="09120-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="09120-121">-VirtualNetworkName</span></span>
<span data-ttu-id="09120-122">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09120-122">The virtual network name.</span></span>

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

### <span data-ttu-id="09120-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09120-123">-Confirm</span></span>
<span data-ttu-id="09120-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09120-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09120-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09120-125">-WhatIf</span></span>
<span data-ttu-id="09120-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09120-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09120-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09120-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09120-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09120-128">CommonParameters</span></span>
<span data-ttu-id="09120-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09120-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09120-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09120-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09120-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09120-131">INPUTS</span></span>

## <span data-ttu-id="09120-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09120-132">OUTPUTS</span></span>

## <span data-ttu-id="09120-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09120-133">NOTES</span></span>

## <span data-ttu-id="09120-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09120-134">RELATED LINKS</span></span>

