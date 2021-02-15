---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114645"
---
# <span data-ttu-id="afb17-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="afb17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afb17-102">SYNOPSIS</span></span>
<span data-ttu-id="afb17-103">Exclui um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="afb17-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="afb17-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afb17-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb17-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="afb17-105">DESCRIPTION</span></span>
<span data-ttu-id="afb17-106">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="afb17-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="afb17-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do gateway no Azure com base no Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="afb17-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="afb17-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="afb17-108">EXAMPLES</span></span>

### <span data-ttu-id="afb17-109">Exemplo 1: Excluir um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="afb17-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="afb17-110">Exclui o objeto do Gateway de Rede Virtual com o nome "myGateway" no grupo de recursos "myRG" Observação: Primeiro, você deve excluir todas as conexões com o Gateway de Rede Virtual usando o cmdlet **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="afb17-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="afb17-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afb17-111">PARAMETERS</span></span>

### <span data-ttu-id="afb17-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afb17-112">-AsJob</span></span>
<span data-ttu-id="afb17-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="afb17-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afb17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb17-114">-DefaultProfile</span></span>
<span data-ttu-id="afb17-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="afb17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afb17-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="afb17-116">-Force</span></span>
<span data-ttu-id="afb17-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="afb17-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afb17-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="afb17-118">-Name</span></span>
<span data-ttu-id="afb17-119">Especifica o nome do gateway de rede virtual que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="afb17-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="afb17-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb17-120">-PassThru</span></span>
<span data-ttu-id="afb17-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="afb17-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="afb17-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="afb17-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="afb17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb17-123">-ResourceGroupName</span></span>
<span data-ttu-id="afb17-124">Especifica o nome do grupo de recursos que contém o gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="afb17-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="afb17-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="afb17-125">-Confirm</span></span>
<span data-ttu-id="afb17-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb17-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb17-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb17-127">-WhatIf</span></span>
<span data-ttu-id="afb17-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="afb17-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb17-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afb17-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb17-130">CommonParameters</span></span>
<span data-ttu-id="afb17-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb17-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afb17-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb17-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="afb17-133">INPUTS</span></span>

### <span data-ttu-id="afb17-134">System.String</span><span class="sxs-lookup"><span data-stu-id="afb17-134">System.String</span></span>

## <span data-ttu-id="afb17-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="afb17-135">OUTPUTS</span></span>

### <span data-ttu-id="afb17-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afb17-136">System.Boolean</span></span>

## <span data-ttu-id="afb17-137">Notas</span><span class="sxs-lookup"><span data-stu-id="afb17-137">NOTES</span></span>

## <span data-ttu-id="afb17-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afb17-138">RELATED LINKS</span></span>

[<span data-ttu-id="afb17-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="afb17-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="afb17-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="afb17-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="afb17-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="afb17-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
