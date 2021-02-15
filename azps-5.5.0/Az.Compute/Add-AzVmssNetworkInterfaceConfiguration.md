---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112153"
---
# <span data-ttu-id="e71f8-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e71f8-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e71f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e71f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e71f8-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="e71f8-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e71f8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e71f8-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e71f8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e71f8-105">DESCRIPTION</span></span>
<span data-ttu-id="e71f8-106">O cmdlet **Add-AzVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e71f8-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e71f8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e71f8-107">EXAMPLES</span></span>

### <span data-ttu-id="e71f8-108">Exemplo 1: Adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="e71f8-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e71f8-109">Esse comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="e71f8-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e71f8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e71f8-110">PARAMETERS</span></span>

### <span data-ttu-id="e71f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71f8-111">-DefaultProfile</span></span>
<span data-ttu-id="e71f8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e71f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71f8-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e71f8-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e71f8-114">Lista de endereços IP do servidor DNS para configurações de dns.</span><span class="sxs-lookup"><span data-stu-id="e71f8-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="e71f8-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="e71f8-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e71f8-116">Especifica se a interface de rede está habilitada para rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="e71f8-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="e71f8-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e71f8-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e71f8-118">Especifica se o encaminhamento de IP está habilitado neste NIC.</span><span class="sxs-lookup"><span data-stu-id="e71f8-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="e71f8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e71f8-119">-Id</span></span>
<span data-ttu-id="e71f8-120">Especifica a ID do Recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e71f8-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e71f8-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e71f8-121">-IpConfiguration</span></span>
<span data-ttu-id="e71f8-122">Especifica as configurações de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e71f8-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="e71f8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e71f8-123">-Name</span></span>
<span data-ttu-id="e71f8-124">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e71f8-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="e71f8-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e71f8-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e71f8-126">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e71f8-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="e71f8-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="e71f8-127">-Primary</span></span>
<span data-ttu-id="e71f8-128">Indica se as interfaces de rede criadas a partir da configuração da interface de rede serão a NIC (central de informações de rede) principal da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e71f8-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="e71f8-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f8-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e71f8-130">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="e71f8-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e71f8-131">Você pode usar [o cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e71f8-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e71f8-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e71f8-132">-Confirm</span></span>
<span data-ttu-id="e71f8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e71f8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71f8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71f8-134">-WhatIf</span></span>
<span data-ttu-id="e71f8-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e71f8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e71f8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e71f8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71f8-137">CommonParameters</span></span>
<span data-ttu-id="e71f8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e71f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71f8-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e71f8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71f8-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="e71f8-140">INPUTS</span></span>

### <span data-ttu-id="e71f8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e71f8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e71f8-142">System.String</span></span>

### <span data-ttu-id="e71f8-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e71f8-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e71f8-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="e71f8-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="e71f8-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e71f8-145">System.String[]</span></span>

## <span data-ttu-id="e71f8-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="e71f8-146">OUTPUTS</span></span>

### <span data-ttu-id="e71f8-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f8-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e71f8-148">Notas</span><span class="sxs-lookup"><span data-stu-id="e71f8-148">NOTES</span></span>

## <span data-ttu-id="e71f8-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e71f8-149">RELATED LINKS</span></span>

[<span data-ttu-id="e71f8-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e71f8-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
