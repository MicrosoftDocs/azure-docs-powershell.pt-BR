---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: f1103e8fc7ed9646aa6b91bc0336e331f7ada990
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258377"
---
# <span data-ttu-id="0e460-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-101">Get-AzVM</span></span>

## <span data-ttu-id="0e460-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e460-102">SYNOPSIS</span></span>
<span data-ttu-id="0e460-103">Obtém as propriedades de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e460-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="0e460-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e460-104">SYNTAX</span></span>

### <span data-ttu-id="0e460-105">Defaultparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e460-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e460-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="0e460-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e460-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="0e460-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e460-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="0e460-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e460-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e460-109">DESCRIPTION</span></span>
<span data-ttu-id="0e460-110">O cmdlet **Get-AzVM** Obtém o modo de exibição de modelo ou o modo de exibição de instância de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e460-110">The **Get-AzVM** cmdlet gets the model view or the instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="0e460-111">O modo de exibição de modelo é a propriedade especificada pelo usuário da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e460-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="0e460-112">O modo de exibição de instância é o status do nível de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e460-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="0e460-113">Especifique o parâmetro *status* para obter o modo de exibição de instância de uma máquina virtual em vez do modo de exibição de modelo que é o padrão.</span><span class="sxs-lookup"><span data-stu-id="0e460-113">Specify the *Status* parameter to get the instance view of a virtual machine instead of the model view which is the default.</span></span>

## <span data-ttu-id="0e460-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e460-114">EXAMPLES</span></span>

### <span data-ttu-id="0e460-115">Exemplo 1: obter propriedades de exibição de modelo e de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="0e460-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="0e460-116">Esse comando obtém as propriedades do modo de exibição de modelo e de exibição de instância da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0e460-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0e460-117">Exemplo 2: obter propriedades do modo de exibição de instância</span><span class="sxs-lookup"><span data-stu-id="0e460-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="0e460-118">Este comando obtém as propriedades da máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0e460-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="0e460-119">Esse comando especifica o parâmetro *status* .</span><span class="sxs-lookup"><span data-stu-id="0e460-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="0e460-120">Portanto, o comando obtém apenas as propriedades do modo de exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="0e460-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="0e460-121">Exemplo 3: obter propriedades de todas as máquinas virtuais em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0e460-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="0e460-122">Esse comando obtém as propriedades de todas as máquinas virtuais no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0e460-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="0e460-123">Exemplo 4: obter todas as máquinas virtuais na sua assinatura</span><span class="sxs-lookup"><span data-stu-id="0e460-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="0e460-124">Este comando obtém todas as máquinas virtuais na sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="0e460-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="0e460-125">Exemplo 5: obter todas as máquinas virtuais no local.</span><span class="sxs-lookup"><span data-stu-id="0e460-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="0e460-126">Esse comando obtém todas as máquinas virtuais na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="0e460-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="0e460-127">Exemplo 6: obter todas as máquinas virtuais usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="0e460-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="0e460-128">Este comando obtém todas as máquinas virtuais na sua assinatura que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="0e460-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="0e460-129">OS</span><span class="sxs-lookup"><span data-stu-id="0e460-129">PARAMETERS</span></span>

### <span data-ttu-id="0e460-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e460-130">-DefaultProfile</span></span>
<span data-ttu-id="0e460-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e460-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e460-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="0e460-132">-DisplayHint</span></span>
<span data-ttu-id="0e460-133">Determina como o objeto de máquina virtual é exibido.</span><span class="sxs-lookup"><span data-stu-id="0e460-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="0e460-134">Os valores válidos são:--Compact: exibe apenas as propriedades de nível superior--expande: exibe todas as propriedades em todos os níveis</span><span class="sxs-lookup"><span data-stu-id="0e460-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e460-135">-Local</span><span class="sxs-lookup"><span data-stu-id="0e460-135">-Location</span></span>
<span data-ttu-id="0e460-136">Especifica um local para as máquinas virtuais a serem listadas.</span><span class="sxs-lookup"><span data-stu-id="0e460-136">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e460-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e460-137">-Name</span></span>
<span data-ttu-id="0e460-138">Especifica o nome da máquina virtual a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="0e460-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0e460-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="0e460-139">-NextLink</span></span>
<span data-ttu-id="0e460-140">Especifica o próximo link.</span><span class="sxs-lookup"><span data-stu-id="0e460-140">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e460-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e460-141">-ResourceGroupName</span></span>
<span data-ttu-id="0e460-142">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e460-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0e460-143">-Status</span><span class="sxs-lookup"><span data-stu-id="0e460-143">-Status</span></span>
<span data-ttu-id="0e460-144">Indica que esse cmdlet obtém apenas o modo de exibição de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0e460-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e460-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e460-145">CommonParameters</span></span>
<span data-ttu-id="0e460-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e460-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e460-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e460-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e460-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e460-148">INPUTS</span></span>

### <span data-ttu-id="0e460-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0e460-149">System.String</span></span>

### <span data-ttu-id="0e460-150">System. URI</span><span class="sxs-lookup"><span data-stu-id="0e460-150">System.Uri</span></span>

### <span data-ttu-id="0e460-151">Microsoft. Azure. Commands. COMPUTE. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="0e460-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="0e460-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e460-152">OUTPUTS</span></span>

### <span data-ttu-id="0e460-153">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e460-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0e460-154">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="0e460-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="0e460-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e460-155">NOTES</span></span>

## <span data-ttu-id="0e460-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e460-156">RELATED LINKS</span></span>

[<span data-ttu-id="0e460-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="0e460-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0e460-159">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="0e460-160">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="0e460-161">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0e460-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e460-162">Update-AzVM</span></span>](./Update-AzVM.md)


