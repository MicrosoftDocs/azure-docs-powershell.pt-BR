---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431798"
---
# <span data-ttu-id="bcd4f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcd4f-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="bcd4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd4f-103">Adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcd4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcd4f-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcd4f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcd4f-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd4f-106">O cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** adiciona uma configuração de interface de rede ao conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bcd4f-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bcd4f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcd4f-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd4f-108">Exemplo 1: adicionar uma configuração de interface de rede ao VMSS</span><span class="sxs-lookup"><span data-stu-id="bcd4f-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="bcd4f-109">Esse comando adiciona uma configuração de interface de rede ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="bcd4f-110">OS</span><span class="sxs-lookup"><span data-stu-id="bcd4f-110">PARAMETERS</span></span>

### <span data-ttu-id="bcd4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd4f-111">-DefaultProfile</span></span>
<span data-ttu-id="bcd4f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcd4f-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="bcd4f-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="bcd4f-114">Lista de endereços IP de servidor DNS para configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="bcd4f-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="bcd4f-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="bcd4f-116">Especifica se a interface de rede é habilitada para rede acelerada.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcd4f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="bcd4f-117">-Id</span></span>
<span data-ttu-id="bcd4f-118">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bcd4f-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcd4f-119">-IpConfiguration</span></span>
<span data-ttu-id="bcd4f-120">Especifica as configurações de IP da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="bcd4f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcd4f-121">-Name</span></span>
<span data-ttu-id="bcd4f-122">Especifica o nome da configuração da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="bcd4f-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="bcd4f-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="bcd4f-124">ID do grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="bcd4f-125">-Principal</span><span class="sxs-lookup"><span data-stu-id="bcd4f-125">-Primary</span></span>
<span data-ttu-id="bcd4f-126">Indica se as interfaces de rede criadas na configuração da interface de rede serão o centro de informações de rede (NIC) principal da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="bcd4f-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bcd4f-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bcd4f-128">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="bcd4f-129">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bcd4f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcd4f-130">-Confirm</span></span>
<span data-ttu-id="bcd4f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd4f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd4f-132">-WhatIf</span></span>
<span data-ttu-id="bcd4f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcd4f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd4f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd4f-135">CommonParameters</span></span>
<span data-ttu-id="bcd4f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd4f-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd4f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd4f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcd4f-138">INPUTS</span></span>

## <span data-ttu-id="bcd4f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcd4f-139">OUTPUTS</span></span>

###  
<span data-ttu-id="bcd4f-140">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bcd4f-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bcd4f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcd4f-141">NOTES</span></span>

## <span data-ttu-id="bcd4f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcd4f-142">RELATED LINKS</span></span>

[<span data-ttu-id="bcd4f-143">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bcd4f-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
