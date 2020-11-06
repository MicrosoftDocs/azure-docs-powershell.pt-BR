---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602037"
---
# <span data-ttu-id="1a263-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a263-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="1a263-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a263-102">SYNOPSIS</span></span>
<span data-ttu-id="1a263-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="1a263-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a263-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a263-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a263-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a263-105">DESCRIPTION</span></span>
<span data-ttu-id="1a263-106">O cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1a263-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1a263-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a263-107">EXAMPLES</span></span>

### <span data-ttu-id="1a263-108">Exemplo 1: adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="1a263-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="1a263-109">Esse comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="1a263-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="1a263-110">OS</span><span class="sxs-lookup"><span data-stu-id="1a263-110">PARAMETERS</span></span>

### <span data-ttu-id="1a263-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="1a263-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="1a263-112">Lista de endereços IP de servidor DNS para configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="1a263-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a263-113">-ID</span><span class="sxs-lookup"><span data-stu-id="1a263-113">-Id</span></span>
<span data-ttu-id="1a263-114">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a263-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1a263-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a263-115">-IpConfiguration</span></span>
<span data-ttu-id="1a263-116">Especifica as configurações de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="1a263-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="1a263-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a263-117">-Name</span></span>
<span data-ttu-id="1a263-118">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="1a263-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="1a263-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1a263-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1a263-120">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="1a263-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="1a263-121">-Principal</span><span class="sxs-lookup"><span data-stu-id="1a263-121">-Primary</span></span>
<span data-ttu-id="1a263-122">Indica se as interfaces de rede criadas na configuração da interface de rede serão o centro de informações de rede (NIC) principal da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a263-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="1a263-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1a263-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1a263-124">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="1a263-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="1a263-125">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1a263-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a263-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a263-126">-Confirm</span></span>
<span data-ttu-id="1a263-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a263-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a263-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a263-128">-WhatIf</span></span>
<span data-ttu-id="1a263-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a263-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a263-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a263-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a263-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a263-131">CommonParameters</span></span>
<span data-ttu-id="1a263-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a263-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a263-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a263-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a263-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a263-134">INPUTS</span></span>

### <span data-ttu-id="1a263-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1a263-135">None</span></span>
<span data-ttu-id="1a263-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1a263-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a263-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a263-137">OUTPUTS</span></span>

###  
<span data-ttu-id="1a263-138">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1a263-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1a263-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a263-139">NOTES</span></span>

## <span data-ttu-id="1a263-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a263-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a263-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1a263-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
