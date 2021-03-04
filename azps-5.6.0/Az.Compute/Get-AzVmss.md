---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 4290c178ad1f84400f542c16a2f90c51c654985c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893365"
---
# <span data-ttu-id="82d0b-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-101">Get-AzVmss</span></span>

## <span data-ttu-id="82d0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="82d0b-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="82d0b-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="82d0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="82d0b-104">SYNTAX</span></span>

### <span data-ttu-id="82d0b-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="82d0b-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82d0b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="82d0b-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82d0b-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="82d0b-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d0b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="82d0b-108">DESCRIPTION</span></span>
<span data-ttu-id="82d0b-109">O cmdlet **Get-AzVmss** obtém o modelo e a exibição de instância de um Conjunto de Escala de Máquina Virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="82d0b-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="82d0b-110">O modelo de exibição é as propriedades especificadas pelo usuário do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="82d0b-111">O exemplo de exibição é o status de nível de instância do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="82d0b-112">Especifique *o parâmetro InstanceView* para obter apenas a exibição de instância de um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="82d0b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82d0b-113">EXAMPLES</span></span>

### <span data-ttu-id="82d0b-114">Exemplo 1: Obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="82d0b-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="82d0b-115">Este comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="82d0b-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="82d0b-116">Como o comando não especifica o parâmetro de opção *InstanceView,* o cmdlet obtém a exibição de modelo do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="82d0b-117">Exemplo 2: Obter todas as Vmss em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="82d0b-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="82d0b-118">Obter todas as Vmss no grupo de recursos "Group001"</span><span class="sxs-lookup"><span data-stu-id="82d0b-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="82d0b-119">Exemplo 3: Obter todas as Vmss em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="82d0b-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="82d0b-120">Obter todas as Vmss na assinatura.</span><span class="sxs-lookup"><span data-stu-id="82d0b-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="82d0b-121">Exemplo 4: Obter todas as Vmss usando filtragem</span><span class="sxs-lookup"><span data-stu-id="82d0b-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="82d0b-122">Obter todas as Vmss na assinatura que começam com "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="82d0b-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="82d0b-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="82d0b-123">PARAMETERS</span></span>

### <span data-ttu-id="82d0b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d0b-124">-DefaultProfile</span></span>
<span data-ttu-id="82d0b-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="82d0b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82d0b-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="82d0b-126">-InstanceView</span></span>
<span data-ttu-id="82d0b-127">Indica que esse cmdlet obtém apenas a exibição de instância do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d0b-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="82d0b-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="82d0b-129">Indica que esse cmdlet lista o histórico de atualização do sistema operacional do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82d0b-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82d0b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82d0b-130">-ResourceGroupName</span></span>
<span data-ttu-id="82d0b-131">Especifica o nome do Grupo de Recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="82d0b-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="82d0b-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="82d0b-132">-VMScaleSetName</span></span>
<span data-ttu-id="82d0b-133">Especiem o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="82d0b-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="82d0b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d0b-134">CommonParameters</span></span>
<span data-ttu-id="82d0b-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d0b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d0b-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82d0b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d0b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82d0b-137">INPUTS</span></span>

### <span data-ttu-id="82d0b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="82d0b-138">System.String</span></span>

## <span data-ttu-id="82d0b-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="82d0b-139">OUTPUTS</span></span>

### <span data-ttu-id="82d0b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="82d0b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="82d0b-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="82d0b-141">NOTES</span></span>

## <span data-ttu-id="82d0b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82d0b-142">RELATED LINKS</span></span>

[<span data-ttu-id="82d0b-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="82d0b-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="82d0b-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="82d0b-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="82d0b-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="82d0b-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="82d0b-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82d0b-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


