---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111685"
---
# <span data-ttu-id="7ff8c-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7ff8c-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="7ff8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ff8c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff8c-103">Obtém um recurso de configuração de Toque.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="7ff8c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ff8c-104">SYNTAX</span></span>

### <span data-ttu-id="7ff8c-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7ff8c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ff8c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ff8c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ff8c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ff8c-107">DESCRIPTION</span></span>
<span data-ttu-id="7ff8c-108">O cmdlet **Get-AzNetworkInterfaceTapConfig obtém** uma Configuração do Azure Tap para um determinado grupo de recursos, interface de rede e toque no nome de configuração ou lista de configurações de toque em um grupo de recursos e interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="7ff8c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ff8c-109">EXAMPLES</span></span>

### <span data-ttu-id="7ff8c-110">Exemplo 1: Obter todas as configurações de toque para uma determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="7ff8c-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="7ff8c-111">Esse comando obtém configurações de toque adicionadas para a determinada interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="7ff8c-112">Exemplo 2: Obter uma determinada configuração de toque</span><span class="sxs-lookup"><span data-stu-id="7ff8c-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="7ff8c-113">Esse comando obtém uma configuração de toque específica adicionada para a determinada interface de rede.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="7ff8c-114">Exemplo 3: Obter uma determinada configuração de toque</span><span class="sxs-lookup"><span data-stu-id="7ff8c-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="7ff8c-115">Esse comando obtém configurações de toque adicionadas para a interface de rede determinada com o nome começando com "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="7ff8c-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="7ff8c-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ff8c-116">PARAMETERS</span></span>

### <span data-ttu-id="7ff8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff8c-117">-DefaultProfile</span></span>
<span data-ttu-id="7ff8c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ff8c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ff8c-119">-Name</span></span>
<span data-ttu-id="7ff8c-120">Nome da configuração de toque específica.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="7ff8c-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7ff8c-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="7ff8c-122">O nome da Interface de Rede.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="7ff8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ff8c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-124">The resource group name.</span></span>

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

### <span data-ttu-id="7ff8c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ff8c-125">-ResourceId</span></span>
<span data-ttu-id="7ff8c-126">ResourceId do recurso TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ff8c-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="7ff8c-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7ff8c-127">-Confirm</span></span>
<span data-ttu-id="7ff8c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff8c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff8c-129">-WhatIf</span></span>
<span data-ttu-id="7ff8c-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ff8c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff8c-132">CommonParameters</span></span>
<span data-ttu-id="7ff8c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff8c-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ff8c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff8c-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="7ff8c-135">INPUTS</span></span>

### <span data-ttu-id="7ff8c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7ff8c-136">System.String</span></span>

## <span data-ttu-id="7ff8c-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="7ff8c-137">OUTPUTS</span></span>

### <span data-ttu-id="7ff8c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ff8c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="7ff8c-139">Notas</span><span class="sxs-lookup"><span data-stu-id="7ff8c-139">NOTES</span></span>

## <span data-ttu-id="7ff8c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ff8c-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ff8c-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7ff8c-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7ff8c-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7ff8c-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="7ff8c-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7ff8c-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
