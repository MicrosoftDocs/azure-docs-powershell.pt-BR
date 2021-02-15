---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111927"
---
# <span data-ttu-id="4321d-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4321d-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="4321d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4321d-102">SYNOPSIS</span></span>
<span data-ttu-id="4321d-103">Remove uma tarefa do Azure Database Migration Service do Azure.</span><span class="sxs-lookup"><span data-stu-id="4321d-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="4321d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4321d-104">SYNTAX</span></span>

### <span data-ttu-id="4321d-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4321d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4321d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4321d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4321d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4321d-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4321d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4321d-108">DESCRIPTION</span></span>
<span data-ttu-id="4321d-109">O Remove-AzDataMigrationTask cmdlet remove uma tarefa do Azure Database Migration Service do Azure.</span><span class="sxs-lookup"><span data-stu-id="4321d-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="4321d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4321d-110">EXAMPLES</span></span>

### <span data-ttu-id="4321d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4321d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="4321d-112">O exemplo anterior remove uma tarefa do Serviço de Migração de Banco de Dados do Azure chamada TestTask do Azure com base no parâmetro de nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4321d-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="4321d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4321d-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="4321d-114">O exemplo anterior remove uma tarefa do Serviço de Migração de Banco de Dados do Azure com base no objeto PSProjectTask passado.</span><span class="sxs-lookup"><span data-stu-id="4321d-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="4321d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4321d-115">PARAMETERS</span></span>

### <span data-ttu-id="4321d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4321d-116">-DefaultProfile</span></span>
<span data-ttu-id="4321d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4321d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4321d-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4321d-118">-Force</span></span>
<span data-ttu-id="4321d-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="4321d-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4321d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4321d-120">-InputObject</span></span>
<span data-ttu-id="4321d-121">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="4321d-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="4321d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4321d-122">-Name</span></span>
<span data-ttu-id="4321d-123">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4321d-123">The name of the task.</span></span>

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

### <span data-ttu-id="4321d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4321d-124">-PassThru</span></span>
<span data-ttu-id="4321d-125">Retorna um verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="4321d-125">Returns an true/false.</span></span>
<span data-ttu-id="4321d-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="4321d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4321d-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4321d-127">-ProjectName</span></span>
<span data-ttu-id="4321d-128">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="4321d-128">The name of the project.</span></span>

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

### <span data-ttu-id="4321d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4321d-129">-ResourceGroupName</span></span>
<span data-ttu-id="4321d-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4321d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="4321d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4321d-131">-ResourceId</span></span>
<span data-ttu-id="4321d-132">ID do Recurso do Projeto.</span><span class="sxs-lookup"><span data-stu-id="4321d-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="4321d-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4321d-133">-ServiceName</span></span>
<span data-ttu-id="4321d-134">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4321d-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="4321d-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4321d-135">-Confirm</span></span>
<span data-ttu-id="4321d-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4321d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4321d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4321d-137">-WhatIf</span></span>
<span data-ttu-id="4321d-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4321d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4321d-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4321d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4321d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4321d-140">CommonParameters</span></span>
<span data-ttu-id="4321d-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4321d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4321d-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4321d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4321d-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="4321d-143">INPUTS</span></span>

### <span data-ttu-id="4321d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4321d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="4321d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4321d-145">System.String</span></span>

## <span data-ttu-id="4321d-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="4321d-146">OUTPUTS</span></span>

### <span data-ttu-id="4321d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4321d-147">System.Boolean</span></span>

## <span data-ttu-id="4321d-148">Notas</span><span class="sxs-lookup"><span data-stu-id="4321d-148">NOTES</span></span>

## <span data-ttu-id="4321d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4321d-149">RELATED LINKS</span></span>
