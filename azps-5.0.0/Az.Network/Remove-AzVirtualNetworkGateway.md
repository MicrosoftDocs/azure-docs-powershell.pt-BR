---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284267"
---
# <span data-ttu-id="49037-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="49037-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49037-102">SYNOPSIS</span></span>
<span data-ttu-id="49037-103">Exclui um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="49037-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="49037-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49037-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49037-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49037-105">DESCRIPTION</span></span>
<span data-ttu-id="49037-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="49037-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="49037-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49037-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="49037-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49037-108">EXAMPLES</span></span>

### <span data-ttu-id="49037-109">Exemplo 1: excluir um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="49037-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="49037-110">Exclui o objeto do gateway de rede virtual com o nome "mygateway" dentro do grupo de recursos "myRG" Observação: você deve primeiro excluir todas as conexões com o gateway de rede virtual usando o cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="49037-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="49037-111">OS</span><span class="sxs-lookup"><span data-stu-id="49037-111">PARAMETERS</span></span>

### <span data-ttu-id="49037-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49037-112">-AsJob</span></span>
<span data-ttu-id="49037-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49037-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49037-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49037-114">-DefaultProfile</span></span>
<span data-ttu-id="49037-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49037-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49037-116">-Force</span><span class="sxs-lookup"><span data-stu-id="49037-116">-Force</span></span>
<span data-ttu-id="49037-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="49037-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49037-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="49037-118">-Name</span></span>
<span data-ttu-id="49037-119">Especifica o nome do gateway de rede virtual que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="49037-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49037-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49037-120">-PassThru</span></span>
<span data-ttu-id="49037-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="49037-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49037-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="49037-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49037-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49037-123">-ResourceGroupName</span></span>
<span data-ttu-id="49037-124">Especifica o nome do grupo de recursos que contém o gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="49037-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="49037-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="49037-125">-Confirm</span></span>
<span data-ttu-id="49037-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49037-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49037-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49037-127">-WhatIf</span></span>
<span data-ttu-id="49037-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="49037-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49037-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49037-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49037-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49037-130">CommonParameters</span></span>
<span data-ttu-id="49037-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49037-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49037-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49037-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49037-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49037-133">INPUTS</span></span>

### <span data-ttu-id="49037-134">System. String</span><span class="sxs-lookup"><span data-stu-id="49037-134">System.String</span></span>

## <span data-ttu-id="49037-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49037-135">OUTPUTS</span></span>

### <span data-ttu-id="49037-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49037-136">System.Boolean</span></span>

## <span data-ttu-id="49037-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49037-137">NOTES</span></span>

## <span data-ttu-id="49037-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49037-138">RELATED LINKS</span></span>

[<span data-ttu-id="49037-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49037-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49037-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49037-142">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="49037-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="49037-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
