---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775023"
---
# <span data-ttu-id="c8fdd-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="c8fdd-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="c8fdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fdd-103">Inicia um trabalho de migração de contêiner para migrar contêineres para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="c8fdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8fdd-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8fdd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="c8fdd-106">Inicia um trabalho de migração de contêiner para migrar contêineres para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="c8fdd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="c8fdd-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="c8fdd-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="c8fdd-109">Inicia uma migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-109">Starts a container migration.</span></span>

## <span data-ttu-id="c8fdd-110">OS</span><span class="sxs-lookup"><span data-stu-id="c8fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="c8fdd-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8fdd-111">-StorageAccountName</span></span>
<span data-ttu-id="c8fdd-112">O nome da conta de armazenamento na qual o contêiner localiza.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c8fdd-113">-ContainerName</span></span>
<span data-ttu-id="c8fdd-114">O nome do contêiner a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-115">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c8fdd-115">-ShareName</span></span>
<span data-ttu-id="c8fdd-116">Nome do compartilhamento que contém o contêiner especificado para a migração.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8fdd-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8fdd-118">O nome do grupo de recursos no qual o provedor de recursos de armazenamento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-119">-Farmname</span><span class="sxs-lookup"><span data-stu-id="c8fdd-119">-FarmName</span></span>
<span data-ttu-id="c8fdd-120">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="c8fdd-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="c8fdd-122">O caminho UNC do compartilhamento de destino para a migração.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8fdd-123">-AsJob</span></span>
<span data-ttu-id="c8fdd-124">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c8fdd-125">-Force</span></span>
<span data-ttu-id="c8fdd-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8fdd-127">-WhatIf</span></span>
<span data-ttu-id="c8fdd-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8fdd-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8fdd-130">-Confirm</span></span>
<span data-ttu-id="c8fdd-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8fdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fdd-132">CommonParameters</span></span>
<span data-ttu-id="c8fdd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8fdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fdd-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8fdd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fdd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8fdd-135">INPUTS</span></span>

## <span data-ttu-id="c8fdd-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8fdd-136">OUTPUTS</span></span>

## <span data-ttu-id="c8fdd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8fdd-137">NOTES</span></span>

## <span data-ttu-id="c8fdd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8fdd-138">RELATED LINKS</span></span>
