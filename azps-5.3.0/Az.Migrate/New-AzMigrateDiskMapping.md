---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272687"
---
# <span data-ttu-id="dbf2c-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="dbf2c-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="dbf2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf2c-103">Cria um novo mapeamento de disco</span><span class="sxs-lookup"><span data-stu-id="dbf2c-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="dbf2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbf2c-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="dbf2c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbf2c-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf2c-106">O cmdlet New-AzMigrateDiskMapping cria um mapeamento do disco de origem conectado ao servidor a ser migrado</span><span class="sxs-lookup"><span data-stu-id="dbf2c-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="dbf2c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbf2c-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf2c-108">Exemplo 1: criar discos</span><span class="sxs-lookup"><span data-stu-id="dbf2c-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="dbf2c-109">Objeto obter discos para fornecer entrada para New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="dbf2c-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="dbf2c-110">OS</span><span class="sxs-lookup"><span data-stu-id="dbf2c-110">PARAMETERS</span></span>

### <span data-ttu-id="dbf2c-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="dbf2c-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="dbf2c-112">Especifica o conjunto de encyption de disco a ser usado.</span><span class="sxs-lookup"><span data-stu-id="dbf2c-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="dbf2c-113">-DiskId</span><span class="sxs-lookup"><span data-stu-id="dbf2c-113">-DiskID</span></span>
<span data-ttu-id="dbf2c-114">Especifica a identificação do disco conectado ao servidor descoberto a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="dbf2c-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="dbf2c-115">-Disktype</span><span class="sxs-lookup"><span data-stu-id="dbf2c-115">-DiskType</span></span>
<span data-ttu-id="dbf2c-116">Especifica o tipo de disco a ser usado para a VM do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf2c-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="dbf2c-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="dbf2c-117">-IsOSDisk</span></span>
<span data-ttu-id="dbf2c-118">Especifica se o disco contém o sistema operacional para o servidor de origem a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="dbf2c-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="dbf2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf2c-119">CommonParameters</span></span>
<span data-ttu-id="dbf2c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf2c-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbf2c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf2c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbf2c-122">INPUTS</span></span>

## <span data-ttu-id="dbf2c-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbf2c-123">OUTPUTS</span></span>

### <span data-ttu-id="dbf2c-124">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="dbf2c-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="dbf2c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbf2c-125">NOTES</span></span>

<span data-ttu-id="dbf2c-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dbf2c-126">ALIASES</span></span>

## <span data-ttu-id="dbf2c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbf2c-127">RELATED LINKS</span></span>

