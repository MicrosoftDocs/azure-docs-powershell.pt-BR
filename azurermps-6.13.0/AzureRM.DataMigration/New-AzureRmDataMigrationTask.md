---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440056"
---
# <span data-ttu-id="84986-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="84986-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="84986-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84986-102">SYNOPSIS</span></span>
<span data-ttu-id="84986-103">Cria e inicia uma tarefa de migração de dados no serviço de migração de banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="84986-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84986-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84986-104">SYNTAX</span></span>

### <span data-ttu-id="84986-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="84986-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84986-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84986-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84986-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84986-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84986-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84986-108">DESCRIPTION</span></span>
<span data-ttu-id="84986-109">O cmdlet New-AzureRmDataMigrationTask cria uma tarefa de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="84986-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="84986-110">Esse cmdlet tem parâmetros para enumerador de tipo de tarefa, grupo de recursos do Azure, nome do serviço de migração de banco de dados do Azure associado e projeto como entrada.</span><span class="sxs-lookup"><span data-stu-id="84986-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="84986-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84986-111">EXAMPLES</span></span>

### <span data-ttu-id="84986-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84986-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="84986-113">Este script de exemplo mostra como criar uma nova tarefa de migração de dados chamada MyMigrationTask no projeto chamado myDMSProject e Service chamado TestService.</span><span class="sxs-lookup"><span data-stu-id="84986-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="84986-114">OS</span><span class="sxs-lookup"><span data-stu-id="84986-114">PARAMETERS</span></span>

### <span data-ttu-id="84986-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84986-115">-DefaultProfile</span></span>
<span data-ttu-id="84986-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84986-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84986-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84986-117">-InputObject</span></span>
<span data-ttu-id="84986-118">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="84986-118">PSProject Object.</span></span>

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

### <span data-ttu-id="84986-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="84986-119">-Name</span></span>
<span data-ttu-id="84986-120">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="84986-120">The name of the task.</span></span>

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

### <span data-ttu-id="84986-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="84986-121">-ProjectName</span></span>
<span data-ttu-id="84986-122">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="84986-122">The name of the project.</span></span>

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

### <span data-ttu-id="84986-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84986-123">-ResourceGroupName</span></span>
<span data-ttu-id="84986-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84986-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="84986-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84986-125">-ResourceId</span></span>
<span data-ttu-id="84986-126">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="84986-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="84986-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="84986-127">-ServiceName</span></span>
<span data-ttu-id="84986-128">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="84986-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="84986-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="84986-129">-TaskType</span></span>
<span data-ttu-id="84986-130">Tipo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="84986-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84986-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84986-131">-Confirm</span></span>
<span data-ttu-id="84986-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84986-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84986-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84986-133">-WhatIf</span></span>
<span data-ttu-id="84986-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84986-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84986-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84986-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84986-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84986-136">CommonParameters</span></span>
<span data-ttu-id="84986-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84986-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84986-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84986-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84986-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84986-139">INPUTS</span></span>

### <span data-ttu-id="84986-140">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="84986-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="84986-141">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84986-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="84986-142">System. String</span><span class="sxs-lookup"><span data-stu-id="84986-142">System.String</span></span>

## <span data-ttu-id="84986-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84986-143">OUTPUTS</span></span>

### <span data-ttu-id="84986-144">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="84986-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="84986-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84986-145">NOTES</span></span>

## <span data-ttu-id="84986-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84986-146">RELATED LINKS</span></span>
