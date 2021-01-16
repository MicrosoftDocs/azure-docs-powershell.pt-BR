---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258287"
---
# <span data-ttu-id="a25a1-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a25a1-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="a25a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a25a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a25a1-103">Remove uma configuração de toque de determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="a25a1-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="a25a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a25a1-104">SYNTAX</span></span>

### <span data-ttu-id="a25a1-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a25a1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25a1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25a1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25a1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25a1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a25a1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a25a1-108">DESCRIPTION</span></span>
<span data-ttu-id="a25a1-109">O cmdlet **Remove-AzNetworkInterfaceTapConfig** remove uma configuração do Azure Tap de uma lista de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a25a1-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="a25a1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a25a1-110">EXAMPLES</span></span>

### <span data-ttu-id="a25a1-111">Exemplo 1: remover uma configuração de toque</span><span class="sxs-lookup"><span data-stu-id="a25a1-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="a25a1-112">Esse comando Remove o TapConfiguration do NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a25a1-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="a25a1-113">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="a25a1-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="a25a1-114">Exemplo 2: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="a25a1-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="a25a1-115">Esse comando Remove o TapConfiguration do NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a25a1-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="a25a1-116">Como o parâmetro *Force* é usado, o usuário não será solicitado a confirmar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="a25a1-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="a25a1-117">OS</span><span class="sxs-lookup"><span data-stu-id="a25a1-117">PARAMETERS</span></span>

### <span data-ttu-id="a25a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25a1-118">-DefaultProfile</span></span>
<span data-ttu-id="a25a1-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a25a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a25a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a25a1-120">-Force</span></span>
<span data-ttu-id="a25a1-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a25a1-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a25a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a25a1-122">-InputObject</span></span>
<span data-ttu-id="a25a1-123">Referência a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="a25a1-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a25a1-124">-Name</span></span>
<span data-ttu-id="a25a1-125">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a25a1-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-126">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="a25a1-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="a25a1-127">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a25a1-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a25a1-128">-PassThru</span></span>
<span data-ttu-id="a25a1-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a25a1-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a25a1-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a25a1-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a25a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="a25a1-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a25a1-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a25a1-133">-ResourceId</span></span>
<span data-ttu-id="a25a1-134">NetworkInterfaceTapConfig ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a25a1-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a25a1-135">-Confirm</span></span>
<span data-ttu-id="a25a1-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25a1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25a1-137">-WhatIf</span></span>
<span data-ttu-id="a25a1-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a25a1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a25a1-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a25a1-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25a1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25a1-140">CommonParameters</span></span>
<span data-ttu-id="a25a1-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25a1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25a1-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25a1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25a1-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a25a1-143">INPUTS</span></span>

### <span data-ttu-id="a25a1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a25a1-144">System.String</span></span>

### <span data-ttu-id="a25a1-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="a25a1-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="a25a1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a25a1-146">OUTPUTS</span></span>

### <span data-ttu-id="a25a1-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a25a1-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a25a1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a25a1-148">NOTES</span></span>

## <span data-ttu-id="a25a1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a25a1-149">RELATED LINKS</span></span>

[<span data-ttu-id="a25a1-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a25a1-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a25a1-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a25a1-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a25a1-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a25a1-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
