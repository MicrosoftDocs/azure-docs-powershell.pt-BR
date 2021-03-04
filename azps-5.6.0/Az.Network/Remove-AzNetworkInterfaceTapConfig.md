---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 54468717f979188d31d6ba318556be87c37e50b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890756"
---
# <span data-ttu-id="5156b-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5156b-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="5156b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5156b-102">SYNOPSIS</span></span>
<span data-ttu-id="5156b-103">Remove uma configuração de toque de uma determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="5156b-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="5156b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5156b-104">SYNTAX</span></span>

### <span data-ttu-id="5156b-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5156b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5156b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5156b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5156b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5156b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5156b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5156b-108">DESCRIPTION</span></span>
<span data-ttu-id="5156b-109">O cmdlet **Remove-AzNetworkInterfaceTapConfig** remove uma configuração de toque do Azure de uma lista de interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="5156b-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="5156b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5156b-110">EXAMPLES</span></span>

### <span data-ttu-id="5156b-111">Exemplo 1: Remover uma configuração de toque</span><span class="sxs-lookup"><span data-stu-id="5156b-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="5156b-112">Este comando remove o TapConfiguration de NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5156b-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="5156b-113">Como o *parâmetro Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="5156b-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="5156b-114">Exemplo 2: Remover uma interface de rede</span><span class="sxs-lookup"><span data-stu-id="5156b-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="5156b-115">Este comando remove o TapConfiguration de NetworkInterface1 em um grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="5156b-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="5156b-116">Como o *parâmetro Force* é usado, o usuário não é solicitado a confirmar.</span><span class="sxs-lookup"><span data-stu-id="5156b-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="5156b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5156b-117">PARAMETERS</span></span>

### <span data-ttu-id="5156b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5156b-118">-DefaultProfile</span></span>
<span data-ttu-id="5156b-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5156b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5156b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5156b-120">-Force</span></span>
<span data-ttu-id="5156b-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5156b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5156b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5156b-122">-InputObject</span></span>
<span data-ttu-id="5156b-123">Referência a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="5156b-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="5156b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5156b-124">-Name</span></span>
<span data-ttu-id="5156b-125">O nome de paração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5156b-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="5156b-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5156b-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="5156b-127">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5156b-127">The virtual network name.</span></span>

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

### <span data-ttu-id="5156b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5156b-128">-PassThru</span></span>
<span data-ttu-id="5156b-129">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5156b-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5156b-130">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5156b-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5156b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5156b-131">-ResourceGroupName</span></span>
<span data-ttu-id="5156b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5156b-132">The resource group name.</span></span>

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

### <span data-ttu-id="5156b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5156b-133">-ResourceId</span></span>
<span data-ttu-id="5156b-134">ID de recurso NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="5156b-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="5156b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5156b-135">-Confirm</span></span>
<span data-ttu-id="5156b-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5156b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5156b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5156b-137">-WhatIf</span></span>
<span data-ttu-id="5156b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5156b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5156b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5156b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5156b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5156b-140">CommonParameters</span></span>
<span data-ttu-id="5156b-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5156b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5156b-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5156b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5156b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5156b-143">INPUTS</span></span>

### <span data-ttu-id="5156b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5156b-144">System.String</span></span>

### <span data-ttu-id="5156b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="5156b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="5156b-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5156b-146">OUTPUTS</span></span>

### <span data-ttu-id="5156b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5156b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="5156b-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="5156b-148">NOTES</span></span>

## <span data-ttu-id="5156b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5156b-149">RELATED LINKS</span></span>

[<span data-ttu-id="5156b-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5156b-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5156b-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5156b-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="5156b-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5156b-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
