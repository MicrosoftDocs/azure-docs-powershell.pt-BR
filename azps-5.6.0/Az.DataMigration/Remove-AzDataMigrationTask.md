---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: acb7e9b453b94381f4f5a2a0edf49e32258809ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891202"
---
# <span data-ttu-id="f0991-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f0991-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="f0991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0991-102">SYNOPSIS</span></span>
<span data-ttu-id="f0991-103">Remove uma tarefa do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0991-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="f0991-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f0991-104">SYNTAX</span></span>

### <span data-ttu-id="f0991-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f0991-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0991-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0991-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0991-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0991-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0991-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f0991-108">DESCRIPTION</span></span>
<span data-ttu-id="f0991-109">O Remove-AzDataMigrationTask cmdlet remove uma tarefa do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0991-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="f0991-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0991-110">EXAMPLES</span></span>

### <span data-ttu-id="f0991-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0991-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="f0991-112">O exemplo anterior remove uma tarefa do Serviço de Migração de Banco de Dados do Azure chamada TestTask do Azure com base no parâmetro nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0991-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="f0991-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f0991-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="f0991-114">O exemplo anterior remove uma tarefa do Serviço de Migração de Banco de Dados do Azure com base no objeto PSProjectTask passado.</span><span class="sxs-lookup"><span data-stu-id="f0991-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="f0991-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f0991-115">PARAMETERS</span></span>

### <span data-ttu-id="f0991-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0991-116">-DefaultProfile</span></span>
<span data-ttu-id="f0991-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f0991-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0991-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f0991-118">-Force</span></span>
<span data-ttu-id="f0991-119">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f0991-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f0991-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0991-120">-InputObject</span></span>
<span data-ttu-id="f0991-121">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="f0991-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0991-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0991-122">-Name</span></span>
<span data-ttu-id="f0991-123">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f0991-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0991-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0991-124">-PassThru</span></span>
<span data-ttu-id="f0991-125">Retorna um true/false.</span><span class="sxs-lookup"><span data-stu-id="f0991-125">Returns an true/false.</span></span>
<span data-ttu-id="f0991-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f0991-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0991-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f0991-127">-ProjectName</span></span>
<span data-ttu-id="f0991-128">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="f0991-128">The name of the project.</span></span>

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

### <span data-ttu-id="f0991-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0991-129">-ResourceGroupName</span></span>
<span data-ttu-id="f0991-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f0991-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0991-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0991-131">-ResourceId</span></span>
<span data-ttu-id="f0991-132">ID do Recurso do Project.</span><span class="sxs-lookup"><span data-stu-id="f0991-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="f0991-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f0991-133">-ServiceName</span></span>
<span data-ttu-id="f0991-134">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="f0991-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="f0991-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0991-135">-Confirm</span></span>
<span data-ttu-id="f0991-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0991-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0991-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0991-137">-WhatIf</span></span>
<span data-ttu-id="f0991-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0991-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0991-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0991-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0991-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0991-140">CommonParameters</span></span>
<span data-ttu-id="f0991-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0991-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0991-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0991-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0991-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0991-143">INPUTS</span></span>

### <span data-ttu-id="f0991-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="f0991-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="f0991-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f0991-145">System.String</span></span>

## <span data-ttu-id="f0991-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f0991-146">OUTPUTS</span></span>

### <span data-ttu-id="f0991-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0991-147">System.Boolean</span></span>

## <span data-ttu-id="f0991-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="f0991-148">NOTES</span></span>

## <span data-ttu-id="f0991-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0991-149">RELATED LINKS</span></span>
