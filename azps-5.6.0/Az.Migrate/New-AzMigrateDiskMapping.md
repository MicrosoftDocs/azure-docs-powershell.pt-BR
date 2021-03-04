---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889233"
---
# <span data-ttu-id="c8b4e-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="c8b4e-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="c8b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b4e-103">Cria um novo mapeamento de disco</span><span class="sxs-lookup"><span data-stu-id="c8b4e-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="c8b4e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8b4e-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8b4e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="c8b4e-106">O New-AzMigrateDiskMapping cmdlet cria um mapeamento do disco de origem anexado ao servidor a ser migrado</span><span class="sxs-lookup"><span data-stu-id="c8b4e-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="c8b4e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="c8b4e-108">Exemplo 1: Fazer discos</span><span class="sxs-lookup"><span data-stu-id="c8b4e-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="c8b4e-109">Obter o objeto disks para fornecer entrada para New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c8b4e-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c8b4e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-110">PARAMETERS</span></span>

### <span data-ttu-id="c8b4e-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="c8b4e-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="c8b4e-112">Especifica o conjunto dencyption de disco a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c8b4e-112">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b4e-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="c8b4e-113">-DiskID</span></span>
<span data-ttu-id="c8b4e-114">Especifica a ID de disco do disco anexado ao servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="c8b4e-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b4e-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="c8b4e-115">-DiskType</span></span>
<span data-ttu-id="c8b4e-116">Especifica o tipo de disco a ser usado para a VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b4e-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b4e-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="c8b4e-117">-IsOSDisk</span></span>
<span data-ttu-id="c8b4e-118">Especifica se o disco contém o Sistema Operacional para o servidor de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="c8b4e-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b4e-119">CommonParameters</span></span>
<span data-ttu-id="c8b4e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b4e-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8b4e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b4e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-122">INPUTS</span></span>

## <span data-ttu-id="c8b4e-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-123">OUTPUTS</span></span>

### <span data-ttu-id="c8b4e-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="c8b4e-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="c8b4e-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8b4e-125">NOTES</span></span>

<span data-ttu-id="c8b4e-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c8b4e-126">ALIASES</span></span>

## <span data-ttu-id="c8b4e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8b4e-127">RELATED LINKS</span></span>

