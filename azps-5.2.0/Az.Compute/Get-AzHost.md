---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258163"
---
# <span data-ttu-id="de5cd-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="de5cd-101">Get-AzHost</span></span>

## <span data-ttu-id="de5cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="de5cd-103">Obtenha ou liste os hosts.</span><span class="sxs-lookup"><span data-stu-id="de5cd-103">Get or list hosts.</span></span>

## <span data-ttu-id="de5cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de5cd-104">SYNTAX</span></span>

### <span data-ttu-id="de5cd-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="de5cd-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de5cd-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="de5cd-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de5cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de5cd-107">DESCRIPTION</span></span>
<span data-ttu-id="de5cd-108">Esse cmdlet receberá um host em um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="de5cd-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="de5cd-109">Esse cmdlet também lista todos os hosts em um grupo de hosts se um nome de host não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="de5cd-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="de5cd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de5cd-110">EXAMPLES</span></span>

### <span data-ttu-id="de5cd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de5cd-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="de5cd-112">Esse comando retorna um host.</span><span class="sxs-lookup"><span data-stu-id="de5cd-112">This command returns a host.</span></span>

### <span data-ttu-id="de5cd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de5cd-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="de5cd-114">Esse comando retorna o modo de exibição de instância de um host.</span><span class="sxs-lookup"><span data-stu-id="de5cd-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="de5cd-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="de5cd-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="de5cd-116">Esse comando retorna todos os hosts no grupo host fornecido.</span><span class="sxs-lookup"><span data-stu-id="de5cd-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="de5cd-117">OS</span><span class="sxs-lookup"><span data-stu-id="de5cd-117">PARAMETERS</span></span>

### <span data-ttu-id="de5cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5cd-118">-DefaultProfile</span></span>
<span data-ttu-id="de5cd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de5cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5cd-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="de5cd-120">-HostGroupName</span></span>
<span data-ttu-id="de5cd-121">O nome do grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="de5cd-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5cd-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="de5cd-122">-InstanceView</span></span>
<span data-ttu-id="de5cd-123">Indica que esse cmdlet obtém apenas o modo de exibição de instância do host.</span><span class="sxs-lookup"><span data-stu-id="de5cd-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="de5cd-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="de5cd-124">-Name</span></span>
<span data-ttu-id="de5cd-125">O nome do host.</span><span class="sxs-lookup"><span data-stu-id="de5cd-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="de5cd-127">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="de5cd-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5cd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de5cd-128">-ResourceId</span></span>
<span data-ttu-id="de5cd-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="de5cd-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de5cd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5cd-130">CommonParameters</span></span>
<span data-ttu-id="de5cd-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5cd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5cd-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de5cd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5cd-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de5cd-133">INPUTS</span></span>

### <span data-ttu-id="de5cd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="de5cd-134">System.String</span></span>

## <span data-ttu-id="de5cd-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de5cd-135">OUTPUTS</span></span>

### <span data-ttu-id="de5cd-136">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="de5cd-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="de5cd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de5cd-137">NOTES</span></span>

## <span data-ttu-id="de5cd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de5cd-138">RELATED LINKS</span></span>
