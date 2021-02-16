---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118287"
---
# <span data-ttu-id="6338f-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6338f-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="6338f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6338f-102">SYNOPSIS</span></span>
<span data-ttu-id="6338f-103">Exclui um Gateway de Rede Local</span><span class="sxs-lookup"><span data-stu-id="6338f-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="6338f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6338f-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6338f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6338f-105">DESCRIPTION</span></span>
<span data-ttu-id="6338f-106">O Gateway de Rede Local é o objeto que representa seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="6338f-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="6338f-107">O cmdlet **Remove-AzLocalNetworkGateway** exclui o objeto que representa seu gateway local com base no Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="6338f-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6338f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6338f-108">EXAMPLES</span></span>

### <span data-ttu-id="6338f-109">Exemplo 1: Excluir um Gateway de Rede Local</span><span class="sxs-lookup"><span data-stu-id="6338f-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="6338f-110">Exclui o objeto do Gateway de Rede Local com o nome "myLocalGW" no grupo de recursos "myRG" Observação: Primeiro, você deve excluir todas as conexões com o Gateway de Rede Local usando o cmdlet **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="6338f-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="6338f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6338f-111">PARAMETERS</span></span>

### <span data-ttu-id="6338f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6338f-112">-AsJob</span></span>
<span data-ttu-id="6338f-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6338f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6338f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6338f-114">-DefaultProfile</span></span>
<span data-ttu-id="6338f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6338f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6338f-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6338f-116">-Force</span></span>
<span data-ttu-id="6338f-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6338f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6338f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6338f-118">-Name</span></span>
<span data-ttu-id="6338f-119">Especifica o nome do gateway de rede local que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="6338f-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6338f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6338f-120">-PassThru</span></span>
<span data-ttu-id="6338f-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6338f-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6338f-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="6338f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6338f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6338f-123">-ResourceGroupName</span></span>
<span data-ttu-id="6338f-124">Especifica o nome do grupo de recursos que contém o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="6338f-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="6338f-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6338f-125">-Confirm</span></span>
<span data-ttu-id="6338f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6338f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6338f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6338f-127">-WhatIf</span></span>
<span data-ttu-id="6338f-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6338f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6338f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6338f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6338f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6338f-130">CommonParameters</span></span>
<span data-ttu-id="6338f-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6338f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6338f-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6338f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6338f-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="6338f-133">INPUTS</span></span>

### <span data-ttu-id="6338f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6338f-134">System.String</span></span>

## <span data-ttu-id="6338f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="6338f-135">OUTPUTS</span></span>

### <span data-ttu-id="6338f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6338f-136">System.Boolean</span></span>

## <span data-ttu-id="6338f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="6338f-137">NOTES</span></span>

## <span data-ttu-id="6338f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6338f-138">RELATED LINKS</span></span>

[<span data-ttu-id="6338f-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6338f-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="6338f-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6338f-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="6338f-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6338f-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
