---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262291"
---
# <span data-ttu-id="de035-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="de035-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="de035-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de035-102">SYNOPSIS</span></span>
<span data-ttu-id="de035-103">Cria e inicia uma tarefa de migração de dados no serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="de035-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="de035-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de035-104">SYNTAX</span></span>

### <span data-ttu-id="de035-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="de035-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de035-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de035-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de035-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de035-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de035-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de035-108">DESCRIPTION</span></span>
<span data-ttu-id="de035-109">O cmdlet New-AzDataMigrationTask cria uma tarefa de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="de035-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="de035-110">Esse cmdlet tem parâmetros para enumerador de tipo de tarefa, grupo de recursos do Azure, nome do serviço de migração de banco de dados do Azure associado e projeto como entrada.</span><span class="sxs-lookup"><span data-stu-id="de035-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="de035-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de035-111">EXAMPLES</span></span>

### <span data-ttu-id="de035-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de035-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="de035-113">Este script de exemplo mostra como criar uma nova tarefa de migração de dados chamada MyMigrationTask no projeto chamado myDMSProject e Service chamado TestService.</span><span class="sxs-lookup"><span data-stu-id="de035-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="de035-114">OS</span><span class="sxs-lookup"><span data-stu-id="de035-114">PARAMETERS</span></span>

### <span data-ttu-id="de035-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de035-115">-DefaultProfile</span></span>
<span data-ttu-id="de035-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de035-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de035-117">-InputObject</span></span>
<span data-ttu-id="de035-118">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="de035-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de035-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="de035-119">-Name</span></span>
<span data-ttu-id="de035-120">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="de035-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="de035-121">-ProjectName</span></span>
<span data-ttu-id="de035-122">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="de035-122">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de035-123">-ResourceGroupName</span></span>
<span data-ttu-id="de035-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de035-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de035-125">-ResourceId</span></span>
<span data-ttu-id="de035-126">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="de035-126">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de035-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="de035-127">-ServiceName</span></span>
<span data-ttu-id="de035-128">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="de035-128">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="de035-129">-TaskType</span></span>
<span data-ttu-id="de035-130">Tipo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="de035-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="de035-131">-MigrationValidation</span></span> 
<span data-ttu-id="de035-132">Objeto de resposta de tarefa por chamada de validação, opcional, mas recomendado.</span><span class="sxs-lookup"><span data-stu-id="de035-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="de035-133">-Wait</span></span>
<span data-ttu-id="de035-134">Se deve aguardar a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="de035-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="de035-135">Se o sinalizador estiver definido, verifica a cada um segundos até que a tarefa seja concluída e retorne ao usuário as propriedades da tarefa onde a saída ou o erro pode ser inspecionado.</span><span class="sxs-lookup"><span data-stu-id="de035-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de035-136">-Confirm</span></span>
<span data-ttu-id="de035-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de035-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de035-138">-WhatIf</span></span>
<span data-ttu-id="de035-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de035-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de035-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de035-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de035-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de035-141">CommonParameters</span></span>
<span data-ttu-id="de035-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de035-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de035-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de035-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de035-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de035-144">INPUTS</span></span>

### <span data-ttu-id="de035-145">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="de035-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="de035-146">System. String</span><span class="sxs-lookup"><span data-stu-id="de035-146">System.String</span></span>

## <span data-ttu-id="de035-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de035-147">OUTPUTS</span></span>

### <span data-ttu-id="de035-148">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="de035-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="de035-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de035-149">NOTES</span></span>

## <span data-ttu-id="de035-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de035-150">RELATED LINKS</span></span>
