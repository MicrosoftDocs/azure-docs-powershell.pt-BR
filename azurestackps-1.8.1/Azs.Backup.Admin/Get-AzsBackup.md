---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b51280387ad3eb29f05bee8876765a621e0d07c4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774965"
---
# <span data-ttu-id="1182b-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1182b-101">Get-AzsBackup</span></span>

## <span data-ttu-id="1182b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1182b-102">SYNOPSIS</span></span>
<span data-ttu-id="1182b-103">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="1182b-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1182b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1182b-104">SYNTAX</span></span>

### <span data-ttu-id="1182b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="1182b-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1182b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1182b-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1182b-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="1182b-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="1182b-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="1182b-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1182b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1182b-109">DESCRIPTION</span></span>
<span data-ttu-id="1182b-110">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="1182b-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1182b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1182b-111">EXAMPLES</span></span>

### <span data-ttu-id="1182b-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1182b-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="1182b-113">Obter informações sbout todos os backups do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="1182b-113">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="1182b-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1182b-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="1182b-115">Obter informações para o backup de pilha do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="1182b-115">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="1182b-116">OS</span><span class="sxs-lookup"><span data-stu-id="1182b-116">PARAMETERS</span></span>

### <span data-ttu-id="1182b-117">-Local</span><span class="sxs-lookup"><span data-stu-id="1182b-117">-Location</span></span>
<span data-ttu-id="1182b-118">Local de backup.</span><span class="sxs-lookup"><span data-stu-id="1182b-118">Location backed up.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1182b-119">-Name</span></span>
<span data-ttu-id="1182b-120">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="1182b-120">Name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="1182b-121">-ParentResource</span></span>
<span data-ttu-id="1182b-122">Ao passar um local de backup, você retornará a lista de todos os backups nesse local de backup.</span><span class="sxs-lookup"><span data-stu-id="1182b-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: ParentResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1182b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1182b-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1182b-124">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1182b-125">-ResourceId</span></span>
<span data-ttu-id="1182b-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1182b-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="1182b-127">-Skip</span></span>
<span data-ttu-id="1182b-128">{{Fill Skip Description}}</span><span class="sxs-lookup"><span data-stu-id="1182b-128">{{Fill Skip Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-129">-Início</span><span class="sxs-lookup"><span data-stu-id="1182b-129">-Top</span></span>
<span data-ttu-id="1182b-130">{{Fill Top Description}}</span><span class="sxs-lookup"><span data-stu-id="1182b-130">{{Fill Top Description}}</span></span>

```yaml
Type: Int32
Parameter Sets: List, ParentResource
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1182b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1182b-131">CommonParameters</span></span>
<span data-ttu-id="1182b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1182b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1182b-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1182b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1182b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1182b-134">INPUTS</span></span>

## <span data-ttu-id="1182b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1182b-135">OUTPUTS</span></span>

### <span data-ttu-id="1182b-136">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="1182b-136">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="1182b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1182b-137">NOTES</span></span>

## <span data-ttu-id="1182b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1182b-138">RELATED LINKS</span></span>
