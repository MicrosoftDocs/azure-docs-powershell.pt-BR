---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: f249b20fdae02315511434e4703f741f25b2a295
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127107"
---
# <span data-ttu-id="d11b2-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="d11b2-101">Get-AzDisk</span></span>

## <span data-ttu-id="d11b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d11b2-102">SYNOPSIS</span></span>
<span data-ttu-id="d11b2-103">Obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d11b2-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="d11b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d11b2-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d11b2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d11b2-105">DESCRIPTION</span></span>
<span data-ttu-id="d11b2-106">O **cmdlet Get-AzDisk** obtém as propriedades de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d11b2-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="d11b2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d11b2-107">EXAMPLES</span></span>

### <span data-ttu-id="d11b2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d11b2-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/Disk01
Name               : Disk01
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d11b2-109">Esse comando obtém as propriedades do disco chamado 'Disco01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="d11b2-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d11b2-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d11b2-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d11b2-111">Esse comando obtém as propriedades de todos os discos no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="d11b2-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d11b2-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d11b2-112">Example 3</span></span>
```
PS C:\> Get-AzDisk

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d11b2-113">Esse comando obtém as propriedades de todos os discos sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="d11b2-113">This command gets the properties of all disks under the subscription.</span></span>

### <span data-ttu-id="d11b2-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d11b2-114">Example 4</span></span>
```
PS C:\> Get-AzDisk -Name win_OsDisk*

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d11b2-115">Esse comando obtém as propriedades de todos os discos sob o nome da assinatura começando com win1_OsDisk.</span><span class="sxs-lookup"><span data-stu-id="d11b2-115">This command gets the properties of all disks under the subscription name starting with win1_OsDisk.</span></span>

## <span data-ttu-id="d11b2-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d11b2-116">PARAMETERS</span></span>

### <span data-ttu-id="d11b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11b2-117">-DefaultProfile</span></span>
<span data-ttu-id="d11b2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d11b2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d11b2-119">-Nomedo Disco</span><span class="sxs-lookup"><span data-stu-id="d11b2-119">-DiskName</span></span>
<span data-ttu-id="d11b2-120">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="d11b2-120">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="d11b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="d11b2-122">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d11b2-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d11b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11b2-123">CommonParameters</span></span>
<span data-ttu-id="d11b2-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11b2-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d11b2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11b2-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="d11b2-126">INPUTS</span></span>

### <span data-ttu-id="d11b2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d11b2-127">System.String</span></span>

## <span data-ttu-id="d11b2-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="d11b2-128">OUTPUTS</span></span>

### <span data-ttu-id="d11b2-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="d11b2-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d11b2-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d11b2-130">NOTES</span></span>

## <span data-ttu-id="d11b2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d11b2-131">RELATED LINKS</span></span>
