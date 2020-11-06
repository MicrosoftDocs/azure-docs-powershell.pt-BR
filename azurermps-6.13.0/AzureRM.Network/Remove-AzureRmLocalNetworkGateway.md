---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428048"
---
# <span data-ttu-id="27cc9-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27cc9-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="27cc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="27cc9-103">Exclui um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="27cc9-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27cc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27cc9-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27cc9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="27cc9-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="27cc9-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="27cc9-107">O cmdlet **Remove-AzureRmLocalNetworkGateway** exclui o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27cc9-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="27cc9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27cc9-108">EXAMPLES</span></span>

### <span data-ttu-id="27cc9-109">1: excluir um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="27cc9-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="27cc9-110">Exclui o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG" Observação: você deve primeiro excluir todas as conexões com o gateway de rede local usando o cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="27cc9-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="27cc9-111">OS</span><span class="sxs-lookup"><span data-stu-id="27cc9-111">PARAMETERS</span></span>

### <span data-ttu-id="27cc9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27cc9-112">-AsJob</span></span>
<span data-ttu-id="27cc9-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="27cc9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27cc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cc9-114">-DefaultProfile</span></span>
<span data-ttu-id="27cc9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27cc9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27cc9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="27cc9-116">-Force</span></span>
<span data-ttu-id="27cc9-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="27cc9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27cc9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="27cc9-118">-Name</span></span>
<span data-ttu-id="27cc9-119">Especifica o nome do gateway de rede local que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="27cc9-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27cc9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27cc9-120">-PassThru</span></span>
<span data-ttu-id="27cc9-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="27cc9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="27cc9-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="27cc9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27cc9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27cc9-123">-ResourceGroupName</span></span>
<span data-ttu-id="27cc9-124">Especifica o nome do grupo de recursos que contém o gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="27cc9-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="27cc9-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27cc9-125">-Confirm</span></span>
<span data-ttu-id="27cc9-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27cc9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27cc9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27cc9-127">-WhatIf</span></span>
<span data-ttu-id="27cc9-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27cc9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27cc9-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27cc9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27cc9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cc9-130">CommonParameters</span></span>
<span data-ttu-id="27cc9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27cc9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cc9-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27cc9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cc9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27cc9-133">INPUTS</span></span>

### <span data-ttu-id="27cc9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="27cc9-134">System.String</span></span>

## <span data-ttu-id="27cc9-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27cc9-135">OUTPUTS</span></span>

### <span data-ttu-id="27cc9-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27cc9-136">System.Boolean</span></span>

## <span data-ttu-id="27cc9-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27cc9-137">NOTES</span></span>

## <span data-ttu-id="27cc9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27cc9-138">RELATED LINKS</span></span>

[<span data-ttu-id="27cc9-139">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27cc9-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="27cc9-140">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27cc9-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="27cc9-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27cc9-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


