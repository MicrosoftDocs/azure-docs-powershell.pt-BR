---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786081"
---
# <span data-ttu-id="64227-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="64227-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="64227-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64227-102">SYNOPSIS</span></span>
<span data-ttu-id="64227-103">Exclui um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="64227-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64227-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64227-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64227-105">DESCRIPTION</span></span>
<span data-ttu-id="64227-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="64227-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="64227-107">O cmdlet **Get-AzureRmVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64227-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="64227-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64227-108">EXAMPLES</span></span>

### <span data-ttu-id="64227-109">1: excluir um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="64227-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="64227-110">Exclui o objeto do gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="64227-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="64227-111">Observação: você deve primeiro excluir todas as conexões com o gateway de rede virtual usando o cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="64227-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="64227-112">OS</span><span class="sxs-lookup"><span data-stu-id="64227-112">PARAMETERS</span></span>

### <span data-ttu-id="64227-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64227-113">-AsJob</span></span>
<span data-ttu-id="64227-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="64227-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64227-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64227-115">-DefaultProfile</span></span>
<span data-ttu-id="64227-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64227-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64227-117">-Force</span><span class="sxs-lookup"><span data-stu-id="64227-117">-Force</span></span>
<span data-ttu-id="64227-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="64227-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64227-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="64227-119">-Name</span></span>
<span data-ttu-id="64227-120">Especifica o nome do gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="64227-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64227-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64227-121">-PassThru</span></span>
<span data-ttu-id="64227-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="64227-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="64227-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="64227-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="64227-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64227-124">-ResourceGroupName</span></span>
<span data-ttu-id="64227-125">Especifica o nome do grupo de recursos que contém o gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="64227-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="64227-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64227-126">-Confirm</span></span>
<span data-ttu-id="64227-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64227-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64227-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64227-128">-WhatIf</span></span>
<span data-ttu-id="64227-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64227-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64227-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64227-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64227-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64227-131">CommonParameters</span></span>
<span data-ttu-id="64227-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64227-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64227-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64227-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64227-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64227-134">INPUTS</span></span>

## <span data-ttu-id="64227-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64227-135">OUTPUTS</span></span>

## <span data-ttu-id="64227-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64227-136">NOTES</span></span>

## <span data-ttu-id="64227-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64227-137">RELATED LINKS</span></span>

