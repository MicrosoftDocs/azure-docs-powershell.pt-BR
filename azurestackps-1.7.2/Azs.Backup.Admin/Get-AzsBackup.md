---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 364b22c834ae7476e64f972b289e20d3caa5ba80
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774223"
---
# <span data-ttu-id="71dd5-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="71dd5-101">Get-AzsBackup</span></span>

## <span data-ttu-id="71dd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="71dd5-103">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="71dd5-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="71dd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71dd5-104">SYNTAX</span></span>

### <span data-ttu-id="71dd5-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="71dd5-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="71dd5-106">Obter</span><span class="sxs-lookup"><span data-stu-id="71dd5-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="71dd5-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="71dd5-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="71dd5-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="71dd5-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="71dd5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71dd5-109">DESCRIPTION</span></span>
<span data-ttu-id="71dd5-110">Retorna um backup de um local com base em nome.</span><span class="sxs-lookup"><span data-stu-id="71dd5-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="71dd5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71dd5-111">EXAMPLES</span></span>

### <span data-ttu-id="71dd5-112">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="71dd5-112">EXAMPLE 1</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="71dd5-113">Obter informações sobre todos os backups do Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="71dd5-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="71dd5-114">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="71dd5-114">EXAMPLE 2</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="71dd5-115">Obter informações para o backup de pilha do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="71dd5-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="71dd5-116">OS</span><span class="sxs-lookup"><span data-stu-id="71dd5-116">PARAMETERS</span></span>

### <span data-ttu-id="71dd5-117">-Local</span><span class="sxs-lookup"><span data-stu-id="71dd5-117">-Location</span></span>
<span data-ttu-id="71dd5-118">Local de backup.</span><span class="sxs-lookup"><span data-stu-id="71dd5-118">Location backed up.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="71dd5-119">-Name</span></span>
<span data-ttu-id="71dd5-120">Nome do backup.</span><span class="sxs-lookup"><span data-stu-id="71dd5-120">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="71dd5-121">-ParentResource</span></span>
<span data-ttu-id="71dd5-122">Ao passar um local de backup, você retornará a lista de todos os backups nesse local de backup.</span><span class="sxs-lookup"><span data-stu-id="71dd5-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: ParentResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71dd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="71dd5-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71dd5-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71dd5-125">-ResourceId</span></span>
<span data-ttu-id="71dd5-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="71dd5-126">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-127">-Início</span><span class="sxs-lookup"><span data-stu-id="71dd5-127">-Top</span></span>
<span data-ttu-id="71dd5-128">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71dd5-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="71dd5-129">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="71dd5-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="71dd5-130">-Skip</span></span>
<span data-ttu-id="71dd5-131">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71dd5-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71dd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71dd5-132">CommonParameters</span></span>
<span data-ttu-id="71dd5-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71dd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71dd5-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71dd5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71dd5-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71dd5-135">INPUTS</span></span>

## <span data-ttu-id="71dd5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71dd5-136">OUTPUTS</span></span>

### <span data-ttu-id="71dd5-137">Microsoft. AzureStack. Management. backup. admin. Models. backup</span><span class="sxs-lookup"><span data-stu-id="71dd5-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="71dd5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71dd5-138">NOTES</span></span>

## <span data-ttu-id="71dd5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71dd5-139">RELATED LINKS</span></span>