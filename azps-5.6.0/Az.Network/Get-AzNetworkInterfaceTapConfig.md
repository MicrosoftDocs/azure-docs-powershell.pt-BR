---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1c46cb01a2b30853248ca941cbb61d8b0429fc49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885705"
---
# <span data-ttu-id="a27d7-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a27d7-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="a27d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a27d7-103">Obtém um recurso de configuração tocar.</span><span class="sxs-lookup"><span data-stu-id="a27d7-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="a27d7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a27d7-104">SYNTAX</span></span>

### <span data-ttu-id="a27d7-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a27d7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27d7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a27d7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a27d7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a27d7-107">DESCRIPTION</span></span>
<span data-ttu-id="a27d7-108">O cmdlet **Get-AzNetworkInterfaceTapConfig** obtém uma Configuração de Toque do Azure para um determinado grupo de recursos, interface de rede e nome de configuração de toque ou lista de configurações de toque em um grupo de recursos e interface de rede.</span><span class="sxs-lookup"><span data-stu-id="a27d7-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="a27d7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a27d7-109">EXAMPLES</span></span>

### <span data-ttu-id="a27d7-110">Exemplo 1: Obter todas as configurações de toque para uma determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="a27d7-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="a27d7-111">Esse comando obtém configurações de toque adicionadas para a interface de rede determinada.</span><span class="sxs-lookup"><span data-stu-id="a27d7-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="a27d7-112">Exemplo 2: Obter uma configuração de toque determinada</span><span class="sxs-lookup"><span data-stu-id="a27d7-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="a27d7-113">Este comando obtém configuração de toque específica adicionada para a interface de rede determinada.</span><span class="sxs-lookup"><span data-stu-id="a27d7-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="a27d7-114">Exemplo 3: Obter uma configuração de toque determinada</span><span class="sxs-lookup"><span data-stu-id="a27d7-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="a27d7-115">Este comando obtém configurações de toque adicionadas para a interface de rede determinada com o nome começando com "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="a27d7-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="a27d7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a27d7-116">PARAMETERS</span></span>

### <span data-ttu-id="a27d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27d7-117">-DefaultProfile</span></span>
<span data-ttu-id="a27d7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a27d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27d7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a27d7-119">-Name</span></span>
<span data-ttu-id="a27d7-120">Nome da configuração de toque específica.</span><span class="sxs-lookup"><span data-stu-id="a27d7-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a27d7-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a27d7-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="a27d7-122">O nome da Interface de Rede.</span><span class="sxs-lookup"><span data-stu-id="a27d7-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a27d7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a27d7-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27d7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a27d7-125">-ResourceId</span></span>
<span data-ttu-id="a27d7-126">ResourceId do recurso TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="a27d7-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27d7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a27d7-127">-Confirm</span></span>
<span data-ttu-id="a27d7-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a27d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27d7-129">-WhatIf</span></span>
<span data-ttu-id="a27d7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a27d7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a27d7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a27d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27d7-132">CommonParameters</span></span>
<span data-ttu-id="a27d7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27d7-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a27d7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27d7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a27d7-135">INPUTS</span></span>

### <span data-ttu-id="a27d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a27d7-136">System.String</span></span>

## <span data-ttu-id="a27d7-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a27d7-137">OUTPUTS</span></span>

### <span data-ttu-id="a27d7-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="a27d7-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="a27d7-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="a27d7-139">NOTES</span></span>

## <span data-ttu-id="a27d7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a27d7-140">RELATED LINKS</span></span>

[<span data-ttu-id="a27d7-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a27d7-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a27d7-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a27d7-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a27d7-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a27d7-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
