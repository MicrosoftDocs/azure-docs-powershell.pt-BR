---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772000"
---
# <span data-ttu-id="efc10-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="efc10-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="efc10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efc10-102">SYNOPSIS</span></span>
<span data-ttu-id="efc10-103">Obtém um recurso de configuração do toque.</span><span class="sxs-lookup"><span data-stu-id="efc10-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="efc10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efc10-104">SYNTAX</span></span>

### <span data-ttu-id="efc10-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="efc10-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc10-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc10-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc10-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efc10-107">DESCRIPTION</span></span>
<span data-ttu-id="efc10-108">O cmdlet **Get-AzNetworkInterfaceTapConfig** Obtém uma configuração do Azure TAP para um determinado grupo de recursos, interface de rede e toque em nome de configuração ou lista de configurações de toque em um grupo de recursos e em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="efc10-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="efc10-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efc10-109">EXAMPLES</span></span>

### <span data-ttu-id="efc10-110">Exemplo 1: obter todas as configurações de toque para uma determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="efc10-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="efc10-111">Esse comando obtém configurações de toque adicionadas para a interface de rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="efc10-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="efc10-112">Exemplo 2: obter uma determinada configuração de toque</span><span class="sxs-lookup"><span data-stu-id="efc10-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="efc10-113">Esse comando obtém uma configuração de toque específico adicionada para a interface de rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="efc10-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="efc10-114">Exemplo 3: obter uma determinada configuração de toque</span><span class="sxs-lookup"><span data-stu-id="efc10-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="efc10-115">Esse comando obtém configurações de toque adicionadas para a interface de rede fornecida com o nome que começa com "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="efc10-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="efc10-116">OS</span><span class="sxs-lookup"><span data-stu-id="efc10-116">PARAMETERS</span></span>

### <span data-ttu-id="efc10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc10-117">-DefaultProfile</span></span>
<span data-ttu-id="efc10-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efc10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc10-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc10-119">-Name</span></span>
<span data-ttu-id="efc10-120">Nome da configuração do toque específico.</span><span class="sxs-lookup"><span data-stu-id="efc10-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="efc10-121">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="efc10-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="efc10-122">O nome da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="efc10-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="efc10-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc10-123">-ResourceGroupName</span></span>
<span data-ttu-id="efc10-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="efc10-124">The resource group name.</span></span>

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

### <span data-ttu-id="efc10-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc10-125">-ResourceId</span></span>
<span data-ttu-id="efc10-126">ResourceId do recurso TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc10-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="efc10-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="efc10-127">-Confirm</span></span>
<span data-ttu-id="efc10-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc10-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc10-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc10-129">-WhatIf</span></span>
<span data-ttu-id="efc10-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efc10-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc10-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efc10-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc10-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc10-132">CommonParameters</span></span>
<span data-ttu-id="efc10-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc10-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc10-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efc10-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc10-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efc10-135">INPUTS</span></span>

### <span data-ttu-id="efc10-136">System. String</span><span class="sxs-lookup"><span data-stu-id="efc10-136">System.String</span></span>

## <span data-ttu-id="efc10-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efc10-137">OUTPUTS</span></span>

### <span data-ttu-id="efc10-138">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc10-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="efc10-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efc10-139">NOTES</span></span>

## <span data-ttu-id="efc10-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efc10-140">RELATED LINKS</span></span>

[<span data-ttu-id="efc10-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="efc10-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="efc10-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="efc10-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="efc10-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="efc10-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
