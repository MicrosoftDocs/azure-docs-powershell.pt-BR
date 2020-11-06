---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602649"
---
# <span data-ttu-id="7ea8f-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="7ea8f-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="7ea8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ea8f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea8f-103">Cria e inicia uma tarefa de migração de dados no serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ea8f-104">SYNTAX</span></span>

### <span data-ttu-id="7ea8f-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ea8f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7ea8f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ea8f-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7ea8f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ea8f-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7ea8f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ea8f-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea8f-109">O cmdlet New-AzureRmDataMigrationTask cria uma tarefa de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="7ea8f-110">Esse cmdlet tem parâmetros para o enumerador de tipo de tarefa, o grupo de recursos do Azure, o nome do serviço de migração de dados do Azure associado e o projeto como entrada.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="7ea8f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ea8f-111">EXAMPLES</span></span>

### <span data-ttu-id="7ea8f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ea8f-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="7ea8f-113">Este script de exemplo mostra como criar uma nova tarefa de migração de dados chamada MyMigrationTask no projeto chamado myDMSProject e Service chamado TestService.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="7ea8f-114">OS</span><span class="sxs-lookup"><span data-stu-id="7ea8f-114">PARAMETERS</span></span>

### <span data-ttu-id="7ea8f-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ea8f-115">-Confirm</span></span>
<span data-ttu-id="7ea8f-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea8f-117">-DefaultProfile</span></span>
<span data-ttu-id="7ea8f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ea8f-119">-InputObject</span></span>
<span data-ttu-id="7ea8f-120">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ea8f-121">-Name</span></span>
<span data-ttu-id="7ea8f-122">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="7ea8f-123">-ProjectName</span></span>
<span data-ttu-id="7ea8f-124">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ea8f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea8f-127">-ResourceId</span></span>
<span data-ttu-id="7ea8f-128">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7ea8f-129">-ServiceName</span></span>
<span data-ttu-id="7ea8f-130">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="7ea8f-131">-TaskType</span></span>
<span data-ttu-id="7ea8f-132">Tipo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea8f-133">-WhatIf</span></span>
<span data-ttu-id="7ea8f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea8f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ea8f-135">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="7ea8f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ea8f-136">INPUTS</span></span>

### <span data-ttu-id="7ea8f-137">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="7ea8f-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="7ea8f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea8f-138">System.String</span></span>


## <span data-ttu-id="7ea8f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ea8f-139">OUTPUTS</span></span>

### <span data-ttu-id="7ea8f-140">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="7ea8f-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="7ea8f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ea8f-141">NOTES</span></span>

## <span data-ttu-id="7ea8f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ea8f-142">RELATED LINKS</span></span>


