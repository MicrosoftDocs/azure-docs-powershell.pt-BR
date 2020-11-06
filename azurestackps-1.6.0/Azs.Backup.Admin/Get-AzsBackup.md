---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb306ed03cb9ab1f06209345474b2ef196d9e1d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426111"
---
# <span data-ttu-id="5d19d-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="5d19d-101">Get-AzsBackup</span></span>

## <span data-ttu-id="5d19d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d19d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d19d-103">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="5d19d-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="5d19d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d19d-104">SYNTAX</span></span>

### <span data-ttu-id="5d19d-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d19d-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d19d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5d19d-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5d19d-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="5d19d-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="5d19d-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="5d19d-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5d19d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d19d-109">DESCRIPTION</span></span>
<span data-ttu-id="5d19d-110">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="5d19d-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="5d19d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d19d-111">EXAMPLES</span></span>

### <span data-ttu-id="5d19d-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5d19d-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="5d19d-113">Obter informações sobre todos os backups do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5d19d-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="5d19d-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5d19d-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="5d19d-115">Obter informações para o backup de pilha do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="5d19d-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="5d19d-116">OS</span><span class="sxs-lookup"><span data-stu-id="5d19d-116">PARAMETERS</span></span>

### <span data-ttu-id="5d19d-117">-Local</span><span class="sxs-lookup"><span data-stu-id="5d19d-117">-Location</span></span>
<span data-ttu-id="5d19d-118">Local de backup.</span><span class="sxs-lookup"><span data-stu-id="5d19d-118">Location backed up.</span></span>

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

### <span data-ttu-id="5d19d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d19d-119">-Name</span></span>
<span data-ttu-id="5d19d-120">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="5d19d-120">Name of the backup.</span></span>

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

### <span data-ttu-id="5d19d-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="5d19d-121">-ParentResource</span></span>
<span data-ttu-id="5d19d-122">Ao passar um local de backup, você retornará a lista de todos os backups nesse local de backup.</span><span class="sxs-lookup"><span data-stu-id="5d19d-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

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

### <span data-ttu-id="5d19d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d19d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d19d-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d19d-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="5d19d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d19d-125">-ResourceId</span></span>
<span data-ttu-id="5d19d-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="5d19d-126">The resource id.</span></span>

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

### <span data-ttu-id="5d19d-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="5d19d-127">-Skip</span></span>
<span data-ttu-id="5d19d-128">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d19d-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5d19d-129">-Início</span><span class="sxs-lookup"><span data-stu-id="5d19d-129">-Top</span></span>
<span data-ttu-id="5d19d-130">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5d19d-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5d19d-131">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="5d19d-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5d19d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d19d-132">CommonParameters</span></span>
<span data-ttu-id="5d19d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d19d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d19d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d19d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d19d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d19d-135">INPUTS</span></span>

## <span data-ttu-id="5d19d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d19d-136">OUTPUTS</span></span>

### <span data-ttu-id="5d19d-137">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="5d19d-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="5d19d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d19d-138">NOTES</span></span>

## <span data-ttu-id="5d19d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d19d-139">RELATED LINKS</span></span>

