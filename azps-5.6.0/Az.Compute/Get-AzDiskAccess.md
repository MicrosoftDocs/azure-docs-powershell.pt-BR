---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887555"
---
# <span data-ttu-id="ed686-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ed686-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="ed686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed686-102">SYNOPSIS</span></span>
<span data-ttu-id="ed686-103">Obtém as propriedades de Acessos de Disco</span><span class="sxs-lookup"><span data-stu-id="ed686-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="ed686-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed686-104">SYNTAX</span></span>

### <span data-ttu-id="ed686-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed686-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed686-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed686-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed686-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed686-107">DESCRIPTION</span></span>
<span data-ttu-id="ed686-108">O cmdlet **Get-AzDiskAccess** obtém as propriedades dos Acessos de Disco</span><span class="sxs-lookup"><span data-stu-id="ed686-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="ed686-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed686-109">EXAMPLES</span></span>

### <span data-ttu-id="ed686-110">Exemplo 1: usando o conjunto de parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="ed686-110">Example 1: Using Default Parameter Set</span></span> 
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

<span data-ttu-id="ed686-111">Este comando obtém as propriedades de um recurso de Acesso ao Disco chamado 'DiskAccess01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="ed686-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ed686-112">Exemplo 2: Get-AzDiskAccess por Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ed686-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
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

<span data-ttu-id="ed686-113">Este comando obtém as propriedades de todos os acessos de disco no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="ed686-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="ed686-114">Exemplo 3: Obter todo o Acesso ao Disco</span><span class="sxs-lookup"><span data-stu-id="ed686-114">Example 3: Getting all Disk Access</span></span>
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

<span data-ttu-id="ed686-115">Este comando obtém as propriedades de todos os acessos de disco sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="ed686-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="ed686-116">Exemplo 4: Obter todo o Acesso ao Disco usando Caractere Curinga</span><span class="sxs-lookup"><span data-stu-id="ed686-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
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

<span data-ttu-id="ed686-117">Este comando obtém as propriedades de todos os acessos em disco sob o nome da assinatura, começando com 'DiskAccessMicrosoft'.</span><span class="sxs-lookup"><span data-stu-id="ed686-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="ed686-118">Exemplo 5: Obter Acesso ao Disco usando ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ed686-118">Example 5: Get Disk Access using ResourceId.</span></span>
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

<span data-ttu-id="ed686-119">Este comando obtém as propriedades de um Acesso de Disco com o ResourceId determinado.</span><span class="sxs-lookup"><span data-stu-id="ed686-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="ed686-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed686-120">PARAMETERS</span></span>

### <span data-ttu-id="ed686-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed686-121">-DefaultProfile</span></span>
<span data-ttu-id="ed686-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed686-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed686-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ed686-123">-Name</span></span>
<span data-ttu-id="ed686-124">Especifica o nome de um acesso em disco.</span><span class="sxs-lookup"><span data-stu-id="ed686-124">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="ed686-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed686-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed686-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed686-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ed686-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed686-127">-ResourceId</span></span>
<span data-ttu-id="ed686-128">ID do recurso para o acesso ao disco.</span><span class="sxs-lookup"><span data-stu-id="ed686-128">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="ed686-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed686-129">CommonParameters</span></span>
<span data-ttu-id="ed686-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed686-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed686-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed686-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed686-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed686-132">INPUTS</span></span>

### <span data-ttu-id="ed686-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ed686-133">System.String</span></span>

## <span data-ttu-id="ed686-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed686-134">OUTPUTS</span></span>

### <span data-ttu-id="ed686-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ed686-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="ed686-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed686-136">NOTES</span></span>

## <span data-ttu-id="ed686-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed686-137">RELATED LINKS</span></span>
