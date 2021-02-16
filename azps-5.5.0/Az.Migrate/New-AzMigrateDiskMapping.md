---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117554"
---
# <span data-ttu-id="f4f8a-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="f4f8a-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="f4f8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f8a-103">Cria um novo mapeamento de disco</span><span class="sxs-lookup"><span data-stu-id="f4f8a-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="f4f8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4f8a-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="f4f8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f8a-106">O New-AzMigrateDiskMapping cmdlet cria um mapeamento do disco de origem anexado ao servidor a ser migrado</span><span class="sxs-lookup"><span data-stu-id="f4f8a-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="f4f8a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f8a-108">Exemplo 1: Fazer discos</span><span class="sxs-lookup"><span data-stu-id="f4f8a-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="f4f8a-109">Obter objeto de discos para fornecer entrada para New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="f4f8a-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="f4f8a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4f8a-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f8a-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="f4f8a-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="f4f8a-112">Especifica o conjunto dencyption de disco a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f4f8a-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="f4f8a-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="f4f8a-113">-DiskID</span></span>
<span data-ttu-id="f4f8a-114">Especifica a ID de disco do disco anexado ao servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="f4f8a-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="f4f8a-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="f4f8a-115">-DiskType</span></span>
<span data-ttu-id="f4f8a-116">Especifica o tipo de disco a ser usado para o VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f8a-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8a-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="f4f8a-117">-IsOSDisk</span></span>
<span data-ttu-id="f4f8a-118">Especifica se o disco contém o Sistema Operacional para o servidor de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="f4f8a-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="f4f8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f8a-119">CommonParameters</span></span>
<span data-ttu-id="f4f8a-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f8a-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4f8a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f8a-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f4f8a-122">INPUTS</span></span>

## <span data-ttu-id="f4f8a-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="f4f8a-123">OUTPUTS</span></span>

### <span data-ttu-id="f4f8a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="f4f8a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="f4f8a-125">Notas</span><span class="sxs-lookup"><span data-stu-id="f4f8a-125">NOTES</span></span>

<span data-ttu-id="f4f8a-126">Aliases</span><span class="sxs-lookup"><span data-stu-id="f4f8a-126">ALIASES</span></span>

## <span data-ttu-id="f4f8a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4f8a-127">RELATED LINKS</span></span>

