---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944896"
---
# <span data-ttu-id="8ca45-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca45-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="8ca45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ca45-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca45-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="8ca45-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="8ca45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ca45-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ca45-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ca45-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca45-106">O cmdlet **Add-AzVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8ca45-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8ca45-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ca45-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca45-108">Exemplo 1: adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="8ca45-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="8ca45-109">Esse comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="8ca45-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="8ca45-110">OS</span><span class="sxs-lookup"><span data-stu-id="8ca45-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca45-111">-DefaultProfile</span></span>
<span data-ttu-id="8ca45-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca45-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ca45-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="8ca45-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="8ca45-114">Lista de endereços IP de servidor DNS para configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="8ca45-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="8ca45-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="8ca45-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="8ca45-116">Especifica se a interface de rede é habilitada para rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="8ca45-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="8ca45-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8ca45-117">-EnableIPForwarding</span></span>
<span data-ttu-id="8ca45-118">Especifica se o encaminhamento IP está habilitado nesta NIC.</span><span class="sxs-lookup"><span data-stu-id="8ca45-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="8ca45-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8ca45-119">-Id</span></span>
<span data-ttu-id="8ca45-120">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ca45-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="8ca45-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca45-121">-IpConfiguration</span></span>
<span data-ttu-id="8ca45-122">Especifica as configurações de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8ca45-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="8ca45-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ca45-123">-Name</span></span>
<span data-ttu-id="8ca45-124">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="8ca45-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="8ca45-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8ca45-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8ca45-126">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="8ca45-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="8ca45-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="8ca45-127">-Primary</span></span>
<span data-ttu-id="8ca45-128">Indica se as interfaces de rede criadas na configuração da interface de rede serão o centro de informações de rede (NIC) principal da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ca45-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="8ca45-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ca45-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8ca45-130">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="8ca45-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="8ca45-131">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8ca45-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="8ca45-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ca45-132">-Confirm</span></span>
<span data-ttu-id="8ca45-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ca45-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca45-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca45-134">-WhatIf</span></span>
<span data-ttu-id="8ca45-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ca45-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ca45-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ca45-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca45-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca45-137">CommonParameters</span></span>
<span data-ttu-id="8ca45-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca45-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca45-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ca45-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca45-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ca45-140">INPUTS</span></span>

### <span data-ttu-id="8ca45-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ca45-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8ca45-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca45-142">System.String</span></span>

### <span data-ttu-id="8ca45-143">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ca45-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ca45-144">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="8ca45-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="8ca45-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="8ca45-145">System.String[]</span></span>

## <span data-ttu-id="8ca45-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ca45-146">OUTPUTS</span></span>

### <span data-ttu-id="8ca45-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ca45-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8ca45-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ca45-148">NOTES</span></span>

## <span data-ttu-id="8ca45-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ca45-149">RELATED LINKS</span></span>

[<span data-ttu-id="8ca45-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8ca45-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
