---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282059"
---
# <span data-ttu-id="8aa4c-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8aa4c-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="8aa4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8aa4c-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa4c-103">Obtém as propriedades de acessos a disco</span><span class="sxs-lookup"><span data-stu-id="8aa4c-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="8aa4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8aa4c-104">SYNTAX</span></span>

### <span data-ttu-id="8aa4c-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8aa4c-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8aa4c-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa4c-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa4c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8aa4c-107">DESCRIPTION</span></span>
<span data-ttu-id="8aa4c-108">O cmdlet **Get-AzDiskAccess** Obtém as propriedades de acessos de disco</span><span class="sxs-lookup"><span data-stu-id="8aa4c-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="8aa4c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8aa4c-109">EXAMPLES</span></span>

### <span data-ttu-id="8aa4c-110">Exemplo 1: usando o conjunto de parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="8aa4c-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="8aa4c-111">Este comando obtém as propriedades de um recurso de acesso a disco chamado "DiskAccess01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8aa4c-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8aa4c-112">Exemplo 2: Get-AzDiskAccess por grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8aa4c-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="8aa4c-113">Esse comando obtém as propriedades de todos os acessos de disco no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8aa4c-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="8aa4c-114">Exemplo 3: obtendo todos os acessos ao disco</span><span class="sxs-lookup"><span data-stu-id="8aa4c-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="8aa4c-115">Esse comando obtém as propriedades de todos os acessos de disco na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="8aa4c-116">Exemplo 4: obter todos os acessos de disco usando caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="8aa4c-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="8aa4c-117">Esse comando obtém as propriedades de todos os acessos de disco sob o nome da assinatura, começando com "DiskAccessMicrosoft".</span><span class="sxs-lookup"><span data-stu-id="8aa4c-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="8aa4c-118">Exemplo 5: obter acesso a disco usando ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="8aa4c-119">Esse comando obtém as propriedades de um acesso a disco com o ResourceId fornecido.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="8aa4c-120">OS</span><span class="sxs-lookup"><span data-stu-id="8aa4c-120">PARAMETERS</span></span>

### <span data-ttu-id="8aa4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa4c-121">-DefaultProfile</span></span>
<span data-ttu-id="8aa4c-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa4c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8aa4c-123">-Name</span></span>
<span data-ttu-id="8aa4c-124">Especifica o nome de um acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8aa4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="8aa4c-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8aa4c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8aa4c-127">-ResourceId</span></span>
<span data-ttu-id="8aa4c-128">ID do recurso para o acesso ao seu disco.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa4c-129">CommonParameters</span></span>
<span data-ttu-id="8aa4c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa4c-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aa4c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa4c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8aa4c-132">INPUTS</span></span>

### <span data-ttu-id="8aa4c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8aa4c-133">System.String</span></span>

## <span data-ttu-id="8aa4c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8aa4c-134">OUTPUTS</span></span>

### <span data-ttu-id="8aa4c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8aa4c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8aa4c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8aa4c-136">NOTES</span></span>

## <span data-ttu-id="8aa4c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8aa4c-137">RELATED LINKS</span></span>
