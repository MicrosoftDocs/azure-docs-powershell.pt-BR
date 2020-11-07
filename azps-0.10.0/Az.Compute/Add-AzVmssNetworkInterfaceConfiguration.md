---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777077"
---
# <span data-ttu-id="e4566-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4566-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e4566-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4566-102">SYNOPSIS</span></span>
<span data-ttu-id="e4566-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="e4566-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e4566-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4566-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4566-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4566-105">DESCRIPTION</span></span>
<span data-ttu-id="e4566-106">O cmdlet **Add-AzVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e4566-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e4566-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4566-107">EXAMPLES</span></span>

### <span data-ttu-id="e4566-108">Exemplo 1: adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="e4566-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e4566-109">Esse comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="e4566-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e4566-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4566-110">PARAMETERS</span></span>

### <span data-ttu-id="e4566-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4566-111">-DefaultProfile</span></span>
<span data-ttu-id="e4566-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4566-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e4566-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e4566-114">Lista de endereços IP de servidor DNS para configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="e4566-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="e4566-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e4566-116">Especifica se a interface de rede é habilitada para rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="e4566-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e4566-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e4566-118">Especifica se o encaminhamento IP está habilitado nesta NIC.</span><span class="sxs-lookup"><span data-stu-id="e4566-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e4566-119">-Id</span></span>
<span data-ttu-id="e4566-120">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4566-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4566-121">-IpConfiguration</span></span>
<span data-ttu-id="e4566-122">Especifica as configurações de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e4566-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4566-123">-Name</span></span>
<span data-ttu-id="e4566-124">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e4566-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e4566-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e4566-126">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="e4566-126">Id of the network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="e4566-127">-Primary</span></span>
<span data-ttu-id="e4566-128">Indica se as interfaces de rede criadas na configuração da interface de rede serão o centro de informações de rede (NIC) principal da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4566-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e4566-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e4566-130">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="e4566-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e4566-131">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e4566-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4566-132">-Confirm</span></span>
<span data-ttu-id="e4566-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4566-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4566-134">-WhatIf</span></span>
<span data-ttu-id="e4566-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4566-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4566-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4566-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4566-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4566-137">CommonParameters</span></span>
<span data-ttu-id="e4566-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4566-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4566-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4566-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4566-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4566-140">INPUTS</span></span>

### <span data-ttu-id="e4566-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e4566-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e4566-142">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e4566-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e4566-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4566-143">OUTPUTS</span></span>

###  
<span data-ttu-id="e4566-144">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e4566-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e4566-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4566-145">NOTES</span></span>

## <span data-ttu-id="e4566-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4566-146">RELATED LINKS</span></span>

[<span data-ttu-id="e4566-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e4566-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
