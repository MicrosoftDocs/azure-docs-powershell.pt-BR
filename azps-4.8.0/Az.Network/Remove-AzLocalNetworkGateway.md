---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110466"
---
# <span data-ttu-id="8f860-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f860-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="8f860-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f860-102">SYNOPSIS</span></span>
<span data-ttu-id="8f860-103">Exclui um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="8f860-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="8f860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f860-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f860-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f860-105">DESCRIPTION</span></span>
<span data-ttu-id="8f860-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="8f860-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="8f860-107">O cmdlet **Remove-AzLocalNetworkGateway** exclui o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f860-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8f860-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f860-108">EXAMPLES</span></span>

### <span data-ttu-id="8f860-109">Exemplo 1: excluir um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="8f860-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="8f860-110">Exclui o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" Observação: você deve primeiro excluir todas as conexões com o gateway de rede local usando o cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="8f860-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="8f860-111">OS</span><span class="sxs-lookup"><span data-stu-id="8f860-111">PARAMETERS</span></span>

### <span data-ttu-id="8f860-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f860-112">-AsJob</span></span>
<span data-ttu-id="8f860-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8f860-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f860-114">-DefaultProfile</span></span>
<span data-ttu-id="8f860-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f860-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f860-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8f860-116">-Force</span></span>
<span data-ttu-id="8f860-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8f860-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f860-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f860-118">-Name</span></span>
<span data-ttu-id="8f860-119">Especifica o nome do gateway de rede local que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8f860-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f860-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f860-120">-PassThru</span></span>
<span data-ttu-id="8f860-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8f860-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f860-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8f860-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f860-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f860-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f860-124">Especifica o nome do grupo de recursos que contém o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="8f860-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="8f860-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f860-125">-Confirm</span></span>
<span data-ttu-id="8f860-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f860-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f860-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f860-127">-WhatIf</span></span>
<span data-ttu-id="8f860-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f860-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f860-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f860-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f860-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f860-130">CommonParameters</span></span>
<span data-ttu-id="8f860-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f860-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f860-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f860-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f860-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f860-133">INPUTS</span></span>

### <span data-ttu-id="8f860-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8f860-134">System.String</span></span>

## <span data-ttu-id="8f860-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f860-135">OUTPUTS</span></span>

### <span data-ttu-id="8f860-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f860-136">System.Boolean</span></span>

## <span data-ttu-id="8f860-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f860-137">NOTES</span></span>

## <span data-ttu-id="8f860-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f860-138">RELATED LINKS</span></span>

[<span data-ttu-id="8f860-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f860-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="8f860-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f860-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="8f860-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8f860-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
