---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428900"
---
# <span data-ttu-id="97598-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="97598-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="97598-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97598-102">SYNOPSIS</span></span>
<span data-ttu-id="97598-103">Remove uma configuração de toque de determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="97598-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="97598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97598-104">SYNTAX</span></span>

### <span data-ttu-id="97598-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="97598-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97598-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97598-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97598-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97598-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97598-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97598-108">DESCRIPTION</span></span>
<span data-ttu-id="97598-109">O cmdlet **Remove-AzNetworkInterfaceTapConfig** remove uma configuração do Azure Tap de uma lista de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="97598-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="97598-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97598-110">EXAMPLES</span></span>

### <span data-ttu-id="97598-111">Exemplo 1: remover uma configuração de toque</span><span class="sxs-lookup"><span data-stu-id="97598-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="97598-112">Esse comando Remove o TapConfiguration do NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="97598-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="97598-113">Como o parâmetro *Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="97598-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="97598-114">Exemplo 2: remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="97598-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="97598-115">Esse comando Remove o TapConfiguration do NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="97598-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="97598-116">Como o parâmetro *Force* é usado, o usuário não será solicitado a confirmar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="97598-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="97598-117">OS</span><span class="sxs-lookup"><span data-stu-id="97598-117">PARAMETERS</span></span>

### <span data-ttu-id="97598-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97598-118">-DefaultProfile</span></span>
<span data-ttu-id="97598-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97598-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97598-120">-Force</span><span class="sxs-lookup"><span data-stu-id="97598-120">-Force</span></span>
<span data-ttu-id="97598-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="97598-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="97598-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97598-122">-InputObject</span></span>
<span data-ttu-id="97598-123">Referência a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="97598-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="97598-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="97598-124">-Name</span></span>
<span data-ttu-id="97598-125">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="97598-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="97598-126">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="97598-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="97598-127">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="97598-127">The virtual network name.</span></span>

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

### <span data-ttu-id="97598-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97598-128">-PassThru</span></span>
<span data-ttu-id="97598-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="97598-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97598-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="97598-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97598-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97598-131">-ResourceGroupName</span></span>
<span data-ttu-id="97598-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97598-132">The resource group name.</span></span>

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

### <span data-ttu-id="97598-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97598-133">-ResourceId</span></span>
<span data-ttu-id="97598-134">NetworkInterfaceTapConfig ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="97598-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="97598-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97598-135">-Confirm</span></span>
<span data-ttu-id="97598-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97598-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97598-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97598-137">-WhatIf</span></span>
<span data-ttu-id="97598-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97598-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97598-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97598-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97598-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97598-140">CommonParameters</span></span>
<span data-ttu-id="97598-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97598-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97598-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97598-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97598-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97598-143">INPUTS</span></span>

### <span data-ttu-id="97598-144">System. String</span><span class="sxs-lookup"><span data-stu-id="97598-144">System.String</span></span>

### <span data-ttu-id="97598-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="97598-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="97598-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97598-146">OUTPUTS</span></span>

### <span data-ttu-id="97598-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="97598-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="97598-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97598-148">NOTES</span></span>

## <span data-ttu-id="97598-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97598-149">RELATED LINKS</span></span>

[<span data-ttu-id="97598-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="97598-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="97598-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="97598-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="97598-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="97598-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
