---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112139"
---
# <span data-ttu-id="de2a1-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-101">Get-AzVmss</span></span>

## <span data-ttu-id="de2a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="de2a1-103">Obtém as propriedades de um VMSS.</span><span class="sxs-lookup"><span data-stu-id="de2a1-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="de2a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de2a1-104">SYNTAX</span></span>

### <span data-ttu-id="de2a1-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de2a1-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2a1-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="de2a1-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2a1-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="de2a1-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de2a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de2a1-108">DESCRIPTION</span></span>
<span data-ttu-id="de2a1-109">O **cmdlet Get-AzVmss** obtém o modelo e a exibição de instância de um VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="de2a1-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="de2a1-110">O exibição de modelo é as propriedades especificadas pelo usuário do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="de2a1-111">O exibição de instância é o status de nível de instância do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="de2a1-112">Especifique *o parâmetro InstanceView* para obter apenas a exibição de instância de um conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="de2a1-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de2a1-113">EXAMPLES</span></span>

### <span data-ttu-id="de2a1-114">Exemplo 1: Obter as propriedades de um VMSS</span><span class="sxs-lookup"><span data-stu-id="de2a1-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="de2a1-115">Esse comando obtém as propriedades do VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="de2a1-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="de2a1-116">Como o comando não especifica o parâmetro *de opção InstanceView,* o cmdlet obtém a exibição de modelo do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="de2a1-117">Exemplo 2: Obter todos os Vmss em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de2a1-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="de2a1-118">Obter todos os Vmss no grupo de recursos "Grupo001"</span><span class="sxs-lookup"><span data-stu-id="de2a1-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="de2a1-119">Exemplo 3: Obter todos os Vmss em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="de2a1-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="de2a1-120">Obter todos os Vmss na assinatura.</span><span class="sxs-lookup"><span data-stu-id="de2a1-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="de2a1-121">Exemplo 4: Obter todos os Vmss usando filtragem</span><span class="sxs-lookup"><span data-stu-id="de2a1-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="de2a1-122">Obter todos os Vmss na assinatura que começam com "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="de2a1-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="de2a1-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de2a1-123">PARAMETERS</span></span>

### <span data-ttu-id="de2a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2a1-124">-DefaultProfile</span></span>
<span data-ttu-id="de2a1-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="de2a1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de2a1-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="de2a1-126">-InstanceView</span></span>
<span data-ttu-id="de2a1-127">Indica que esse cmdlet obtém apenas a exibição de instância do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="de2a1-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="de2a1-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="de2a1-129">Indica que esse cmdlet lista o histórico de atualização do sistema operacional do conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de2a1-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="de2a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de2a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="de2a1-131">Especifica o nome do Grupo de Recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="de2a1-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="de2a1-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="de2a1-132">-VMScaleSetName</span></span>
<span data-ttu-id="de2a1-133">Especimos o nome do VMSS.</span><span class="sxs-lookup"><span data-stu-id="de2a1-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="de2a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2a1-134">CommonParameters</span></span>
<span data-ttu-id="de2a1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2a1-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de2a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2a1-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="de2a1-137">INPUTS</span></span>

### <span data-ttu-id="de2a1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="de2a1-138">System.String</span></span>

## <span data-ttu-id="de2a1-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="de2a1-139">OUTPUTS</span></span>

### <span data-ttu-id="de2a1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="de2a1-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="de2a1-141">Notas</span><span class="sxs-lookup"><span data-stu-id="de2a1-141">NOTES</span></span>

## <span data-ttu-id="de2a1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de2a1-142">RELATED LINKS</span></span>

[<span data-ttu-id="de2a1-143">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="de2a1-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="de2a1-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="de2a1-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="de2a1-147">Iniciar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="de2a1-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="de2a1-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="de2a1-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


