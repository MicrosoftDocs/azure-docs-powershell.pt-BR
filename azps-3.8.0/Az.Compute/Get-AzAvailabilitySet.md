---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: d01919008adf8c15fa9b4a0c8144e279a3997a92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944644"
---
# <span data-ttu-id="07096-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07096-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="07096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07096-102">SYNOPSIS</span></span>
<span data-ttu-id="07096-103">Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07096-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="07096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07096-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07096-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07096-105">DESCRIPTION</span></span>
<span data-ttu-id="07096-106">O cmdlet **Get-AzAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07096-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="07096-107">Você pode especificar o nome de um conjunto de disponibilidade específico para obter.</span><span class="sxs-lookup"><span data-stu-id="07096-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="07096-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07096-108">EXAMPLES</span></span>

### <span data-ttu-id="07096-109">Exemplo 1: obter um conjunto de disponibilidade específico</span><span class="sxs-lookup"><span data-stu-id="07096-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="07096-110">Esse comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="07096-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="07096-111">Exemplo 2: obter todos os conjuntos de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="07096-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="07096-112">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="07096-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="07096-113">Exemplo 3: obter todos os conjuntos de disponibilidade com filtragem</span><span class="sxs-lookup"><span data-stu-id="07096-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="07096-114">Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11 que começam com "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="07096-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="07096-115">Exemplo 4: obter todos os conjuntos de disponibilidade com nome começando com AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="07096-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="07096-116">Esse comando obtém todos os conjuntos de disponibilidade que começam com "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="07096-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="07096-117">OS</span><span class="sxs-lookup"><span data-stu-id="07096-117">PARAMETERS</span></span>

### <span data-ttu-id="07096-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07096-118">-DefaultProfile</span></span>
<span data-ttu-id="07096-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07096-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07096-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="07096-120">-Name</span></span>
<span data-ttu-id="07096-121">Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="07096-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="07096-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07096-122">-ResourceGroupName</span></span>
<span data-ttu-id="07096-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07096-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07096-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07096-124">CommonParameters</span></span>
<span data-ttu-id="07096-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07096-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07096-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07096-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07096-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07096-127">INPUTS</span></span>

### <span data-ttu-id="07096-128">System. String</span><span class="sxs-lookup"><span data-stu-id="07096-128">System.String</span></span>

## <span data-ttu-id="07096-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07096-129">OUTPUTS</span></span>

### <span data-ttu-id="07096-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07096-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="07096-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07096-131">NOTES</span></span>

## <span data-ttu-id="07096-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07096-132">RELATED LINKS</span></span>

[<span data-ttu-id="07096-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07096-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="07096-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07096-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


