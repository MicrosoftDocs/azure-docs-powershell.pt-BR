---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcbc31b31558a38e61648a0eb9318f68daf19d2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601689"
---
# <span data-ttu-id="67210-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="67210-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="67210-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67210-102">SYNOPSIS</span></span>
<span data-ttu-id="67210-103">Inicia um trabalho de migração de disco gerenciado para migrar discos gerenciados para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="67210-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="67210-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67210-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="67210-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67210-105">DESCRIPTION</span></span>
<span data-ttu-id="67210-106">Crie um trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="67210-106">Create a disk migration job.</span></span>

## <span data-ttu-id="67210-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67210-107">EXAMPLES</span></span>

### <span data-ttu-id="67210-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="67210-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="67210-109">Iniciar um trabalho de migração de disco gerenciado para os primeiros 20 discos</span><span class="sxs-lookup"><span data-stu-id="67210-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="67210-110">OS</span><span class="sxs-lookup"><span data-stu-id="67210-110">PARAMETERS</span></span>

### <span data-ttu-id="67210-111">-Discos</span><span class="sxs-lookup"><span data-stu-id="67210-111">-Disks</span></span>
<span data-ttu-id="67210-112">Os parâmetros da lista de discos.</span><span class="sxs-lookup"><span data-stu-id="67210-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67210-113">-Local</span><span class="sxs-lookup"><span data-stu-id="67210-113">-Location</span></span>
<span data-ttu-id="67210-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="67210-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67210-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="67210-115">-Name</span></span>
<span data-ttu-id="67210-116">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="67210-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67210-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="67210-117">-TargetShare</span></span>
<span data-ttu-id="67210-118">O nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="67210-118">The target share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67210-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67210-119">CommonParameters</span></span>
<span data-ttu-id="67210-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67210-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67210-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67210-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67210-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67210-122">INPUTS</span></span>

## <span data-ttu-id="67210-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67210-123">OUTPUTS</span></span>

### <span data-ttu-id="67210-124">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="67210-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="67210-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67210-125">NOTES</span></span>

## <span data-ttu-id="67210-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67210-126">RELATED LINKS</span></span>

