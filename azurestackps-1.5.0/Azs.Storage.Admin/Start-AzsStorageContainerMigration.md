---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425609"
---
# <span data-ttu-id="41790-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="41790-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="41790-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41790-102">SYNOPSIS</span></span>
<span data-ttu-id="41790-103">Inicia um trabalho de migração de contêiner para migrar contêineres para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="41790-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="41790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41790-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41790-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41790-105">DESCRIPTION</span></span>
<span data-ttu-id="41790-106">Inicia um trabalho de migração de contêiner para migrar contêineres para o compartilhamento de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="41790-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="41790-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41790-107">EXAMPLES</span></span>

### <span data-ttu-id="41790-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41790-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="41790-109">Inicia uma migração de contêineres.</span><span class="sxs-lookup"><span data-stu-id="41790-109">Starts a container migration.</span></span>

## <span data-ttu-id="41790-110">OS</span><span class="sxs-lookup"><span data-stu-id="41790-110">PARAMETERS</span></span>

### <span data-ttu-id="41790-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41790-111">-AsJob</span></span>
<span data-ttu-id="41790-112">Executar assíncrono como um trabalho e retornar o objeto de trabalho.</span><span class="sxs-lookup"><span data-stu-id="41790-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="41790-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="41790-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="41790-114">O caminho UNC do compartilhamento de destino para a migração.</span><span class="sxs-lookup"><span data-stu-id="41790-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="41790-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="41790-115">-FarmName</span></span>
<span data-ttu-id="41790-116">ID do farm.</span><span class="sxs-lookup"><span data-stu-id="41790-116">Farm Id.</span></span>

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

### <span data-ttu-id="41790-117">-Force</span><span class="sxs-lookup"><span data-stu-id="41790-117">-Force</span></span>
<span data-ttu-id="41790-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="41790-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="41790-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="41790-119">-Name</span></span>
<span data-ttu-id="41790-120">O nome do contêiner a ser migrado.</span><span class="sxs-lookup"><span data-stu-id="41790-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41790-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41790-121">-ResourceGroupName</span></span>
<span data-ttu-id="41790-122">O nome do grupo de recursos no qual o provedor de recursos de armazenamento foi registrado.</span><span class="sxs-lookup"><span data-stu-id="41790-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="41790-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="41790-123">-ShareName</span></span>
<span data-ttu-id="41790-124">Nome do compartilhamento que contém o contêiner especificado para a migração.</span><span class="sxs-lookup"><span data-stu-id="41790-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="41790-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="41790-125">-StorageAccountName</span></span>
<span data-ttu-id="41790-126">O nome da conta de armazenamento na qual o contêiner localiza.</span><span class="sxs-lookup"><span data-stu-id="41790-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="41790-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41790-127">-Confirm</span></span>
<span data-ttu-id="41790-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41790-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41790-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41790-129">-WhatIf</span></span>
<span data-ttu-id="41790-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41790-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41790-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41790-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41790-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41790-132">CommonParameters</span></span>
<span data-ttu-id="41790-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41790-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41790-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41790-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41790-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41790-135">INPUTS</span></span>

## <span data-ttu-id="41790-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41790-136">OUTPUTS</span></span>

## <span data-ttu-id="41790-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41790-137">NOTES</span></span>

## <span data-ttu-id="41790-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41790-138">RELATED LINKS</span></span>

