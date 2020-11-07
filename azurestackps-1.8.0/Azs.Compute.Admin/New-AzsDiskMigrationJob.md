---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774666"
---
# <span data-ttu-id="24c6a-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="24c6a-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="24c6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="24c6a-103">Inicia um trabalho de migração de disco gerenciado para migrar discos gerenciados para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="24c6a-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="24c6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24c6a-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="24c6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="24c6a-106">Crie um trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="24c6a-106">Create a disk migration job.</span></span>

## <span data-ttu-id="24c6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="24c6a-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24c6a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="24c6a-109">Iniciar um trabalho de migração de disco gerenciado para os primeiros 20 discos</span><span class="sxs-lookup"><span data-stu-id="24c6a-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="24c6a-110">OS</span><span class="sxs-lookup"><span data-stu-id="24c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="24c6a-111">-Discos</span><span class="sxs-lookup"><span data-stu-id="24c6a-111">-Disks</span></span>
<span data-ttu-id="24c6a-112">Os parâmetros da lista de discos.</span><span class="sxs-lookup"><span data-stu-id="24c6a-112">The parameters of disk list.</span></span>

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

### <span data-ttu-id="24c6a-113">-Local</span><span class="sxs-lookup"><span data-stu-id="24c6a-113">-Location</span></span>
<span data-ttu-id="24c6a-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="24c6a-114">Location of the resource.</span></span>

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

### <span data-ttu-id="24c6a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="24c6a-115">-Name</span></span>
<span data-ttu-id="24c6a-116">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="24c6a-116">The migration job guid name.</span></span>

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

### <span data-ttu-id="24c6a-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="24c6a-117">-TargetShare</span></span>
<span data-ttu-id="24c6a-118">O nome do compartilhamento de destino.</span><span class="sxs-lookup"><span data-stu-id="24c6a-118">The target share name.</span></span>

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

### <span data-ttu-id="24c6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c6a-119">CommonParameters</span></span>
<span data-ttu-id="24c6a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c6a-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c6a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c6a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24c6a-122">INPUTS</span></span>

## <span data-ttu-id="24c6a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24c6a-123">OUTPUTS</span></span>

### <span data-ttu-id="24c6a-124">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="24c6a-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="24c6a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24c6a-125">NOTES</span></span>

## <span data-ttu-id="24c6a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24c6a-126">RELATED LINKS</span></span>

