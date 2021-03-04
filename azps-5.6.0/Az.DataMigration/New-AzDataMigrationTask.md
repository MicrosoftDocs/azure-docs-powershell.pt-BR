---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890436"
---
# <span data-ttu-id="aed69-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="aed69-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="aed69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed69-102">SYNOPSIS</span></span>
<span data-ttu-id="aed69-103">Cria e inicia uma tarefa de migração de dados no Serviço de Migração de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="aed69-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="aed69-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aed69-104">SYNTAX</span></span>

### <span data-ttu-id="aed69-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aed69-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aed69-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aed69-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aed69-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aed69-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed69-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aed69-108">DESCRIPTION</span></span>
<span data-ttu-id="aed69-109">O cmdlet New-AzDataMigrationTask cria uma tarefa de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="aed69-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="aed69-110">Este cmdlet utiliza parâmetros para enumerador de Tipo de Tarefa, Grupo de Recursos do Azure, nome do Serviço de Migração de Banco de Dados do Azure associado e Project como entrada.</span><span class="sxs-lookup"><span data-stu-id="aed69-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="aed69-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aed69-111">EXAMPLES</span></span>

### <span data-ttu-id="aed69-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aed69-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="aed69-113">Este script de exemplo mostra como criar uma nova Tarefa de Migração de Dados chamada MyMigrationTask no projeto chamado myDMSProject e serviço denominado TestService.</span><span class="sxs-lookup"><span data-stu-id="aed69-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="aed69-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aed69-114">PARAMETERS</span></span>

### <span data-ttu-id="aed69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed69-115">-DefaultProfile</span></span>
<span data-ttu-id="aed69-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aed69-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed69-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aed69-117">-InputObject</span></span>
<span data-ttu-id="aed69-118">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="aed69-118">PSProject Object.</span></span>

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

### <span data-ttu-id="aed69-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aed69-119">-Name</span></span>
<span data-ttu-id="aed69-120">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="aed69-120">The name of the task.</span></span>

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

### <span data-ttu-id="aed69-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="aed69-121">-ProjectName</span></span>
<span data-ttu-id="aed69-122">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="aed69-122">The name of the project.</span></span>

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

### <span data-ttu-id="aed69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed69-123">-ResourceGroupName</span></span>
<span data-ttu-id="aed69-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aed69-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="aed69-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aed69-125">-ResourceId</span></span>
<span data-ttu-id="aed69-126">ID do Recurso do Project.</span><span class="sxs-lookup"><span data-stu-id="aed69-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="aed69-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aed69-127">-ServiceName</span></span>
<span data-ttu-id="aed69-128">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="aed69-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="aed69-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="aed69-129">-TaskType</span></span>
<span data-ttu-id="aed69-130">Tipo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="aed69-130">Task Type.</span></span>

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

### <span data-ttu-id="aed69-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="aed69-131">-MigrationValidation</span></span> 
<span data-ttu-id="aed69-132">Objeto de resposta de tarefa por chamada de validação, opcional, mas recomendado.</span><span class="sxs-lookup"><span data-stu-id="aed69-132">Task response object by validation call, optional but recommended.</span></span>

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

### <span data-ttu-id="aed69-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="aed69-133">-Wait</span></span>
<span data-ttu-id="aed69-134">Se a tarefa deve ser terminada.</span><span class="sxs-lookup"><span data-stu-id="aed69-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="aed69-135">Se o sinalizador for definido, verifique a cada um segundos até que a tarefa seja terminada e retorne ao usuário as propriedades da tarefa onde a saída ou o erro podem ser inspecionados.</span><span class="sxs-lookup"><span data-stu-id="aed69-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
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

### <span data-ttu-id="aed69-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aed69-136">-Confirm</span></span>
<span data-ttu-id="aed69-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aed69-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed69-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed69-138">-WhatIf</span></span>
<span data-ttu-id="aed69-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aed69-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed69-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aed69-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed69-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed69-141">CommonParameters</span></span>
<span data-ttu-id="aed69-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed69-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed69-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed69-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed69-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aed69-144">INPUTS</span></span>

### <span data-ttu-id="aed69-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="aed69-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="aed69-146">System.String</span><span class="sxs-lookup"><span data-stu-id="aed69-146">System.String</span></span>

## <span data-ttu-id="aed69-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aed69-147">OUTPUTS</span></span>

### <span data-ttu-id="aed69-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="aed69-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="aed69-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="aed69-149">NOTES</span></span>

## <span data-ttu-id="aed69-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aed69-150">RELATED LINKS</span></span>
