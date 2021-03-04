---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: c85c4292fcae081e50ba98ff873f967f8e32fbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887580"
---
# <span data-ttu-id="73ea3-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="73ea3-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="73ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="73ea3-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="73ea3-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="73ea3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73ea3-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73ea3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="73ea3-106">O cmdlet **Add-AzVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="73ea3-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="73ea3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="73ea3-108">Exemplo 1: Adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="73ea3-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="73ea3-109">Este comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="73ea3-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="73ea3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73ea3-110">PARAMETERS</span></span>

### <span data-ttu-id="73ea3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ea3-111">-DefaultProfile</span></span>
<span data-ttu-id="73ea3-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="73ea3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73ea3-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="73ea3-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="73ea3-114">Lista de endereços IP do servidor dns para configurações dns.</span><span class="sxs-lookup"><span data-stu-id="73ea3-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="73ea3-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="73ea3-116">Especifica se a interface de rede está acelerada habilitada para rede.</span><span class="sxs-lookup"><span data-stu-id="73ea3-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="73ea3-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="73ea3-117">-EnableIPForwarding</span></span>
<span data-ttu-id="73ea3-118">Especifica se o encaminhamento de IP habilitado nesta NIC.</span><span class="sxs-lookup"><span data-stu-id="73ea3-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="73ea3-119">-Id</span><span class="sxs-lookup"><span data-stu-id="73ea3-119">-Id</span></span>
<span data-ttu-id="73ea3-120">Especifica a ID de Recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73ea3-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="73ea3-121">-IpConfiguration</span></span>
<span data-ttu-id="73ea3-122">Especifica as configurações IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="73ea3-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="73ea3-123">-Name</span></span>
<span data-ttu-id="73ea3-124">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="73ea3-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="73ea3-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="73ea3-126">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="73ea3-126">Id of the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="73ea3-127">-Primary</span></span>
<span data-ttu-id="73ea3-128">Indica se as interfaces de rede criadas a partir da configuração da interface de rede serão o centro de informações de rede principal (NIC) da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73ea3-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73ea3-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="73ea3-130">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="73ea3-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="73ea3-131">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="73ea3-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ea3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73ea3-132">-Confirm</span></span>
<span data-ttu-id="73ea3-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73ea3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ea3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ea3-134">-WhatIf</span></span>
<span data-ttu-id="73ea3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73ea3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73ea3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73ea3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ea3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ea3-137">CommonParameters</span></span>
<span data-ttu-id="73ea3-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ea3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ea3-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73ea3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ea3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73ea3-140">INPUTS</span></span>

### <span data-ttu-id="73ea3-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73ea3-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="73ea3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="73ea3-142">System.String</span></span>

### <span data-ttu-id="73ea3-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="73ea3-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="73ea3-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="73ea3-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="73ea3-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="73ea3-145">System.String[]</span></span>

## <span data-ttu-id="73ea3-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73ea3-146">OUTPUTS</span></span>

### <span data-ttu-id="73ea3-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="73ea3-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="73ea3-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="73ea3-148">NOTES</span></span>

## <span data-ttu-id="73ea3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73ea3-149">RELATED LINKS</span></span>

[<span data-ttu-id="73ea3-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="73ea3-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
