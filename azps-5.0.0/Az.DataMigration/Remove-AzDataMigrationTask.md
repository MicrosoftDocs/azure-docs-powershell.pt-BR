---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280747"
---
# <span data-ttu-id="47af3-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="47af3-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="47af3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47af3-102">SYNOPSIS</span></span>
<span data-ttu-id="47af3-103">Remove uma tarefa do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="47af3-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="47af3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47af3-104">SYNTAX</span></span>

### <span data-ttu-id="47af3-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="47af3-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47af3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47af3-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47af3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47af3-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47af3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47af3-108">DESCRIPTION</span></span>
<span data-ttu-id="47af3-109">O cmdlet Remove-AzDataMigrationTask remove uma tarefa do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="47af3-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="47af3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47af3-110">EXAMPLES</span></span>

### <span data-ttu-id="47af3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47af3-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="47af3-112">O exemplo anterior remove uma tarefa do serviço de migração de banco de dados do Azure chamada Tarefateste do Azure com base no parâmetro nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="47af3-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="47af3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47af3-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="47af3-114">O exemplo anterior remove uma tarefa do serviço de migração de banco de dados do Azure baseada no objeto PSProjectTask transmitido.</span><span class="sxs-lookup"><span data-stu-id="47af3-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="47af3-115">OS</span><span class="sxs-lookup"><span data-stu-id="47af3-115">PARAMETERS</span></span>

### <span data-ttu-id="47af3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47af3-116">-DefaultProfile</span></span>
<span data-ttu-id="47af3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47af3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47af3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="47af3-118">-Force</span></span>
<span data-ttu-id="47af3-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="47af3-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="47af3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47af3-120">-InputObject</span></span>
<span data-ttu-id="47af3-121">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="47af3-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="47af3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="47af3-122">-Name</span></span>
<span data-ttu-id="47af3-123">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="47af3-123">The name of the task.</span></span>

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

### <span data-ttu-id="47af3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47af3-124">-PassThru</span></span>
<span data-ttu-id="47af3-125">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="47af3-125">Returns an true/false.</span></span>
<span data-ttu-id="47af3-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="47af3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="47af3-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="47af3-127">-ProjectName</span></span>
<span data-ttu-id="47af3-128">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="47af3-128">The name of the project.</span></span>

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

### <span data-ttu-id="47af3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47af3-129">-ResourceGroupName</span></span>
<span data-ttu-id="47af3-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47af3-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="47af3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47af3-131">-ResourceId</span></span>
<span data-ttu-id="47af3-132">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="47af3-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="47af3-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="47af3-133">-ServiceName</span></span>
<span data-ttu-id="47af3-134">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47af3-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="47af3-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47af3-135">-Confirm</span></span>
<span data-ttu-id="47af3-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47af3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47af3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47af3-137">-WhatIf</span></span>
<span data-ttu-id="47af3-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47af3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47af3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47af3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47af3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47af3-140">CommonParameters</span></span>
<span data-ttu-id="47af3-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47af3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47af3-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47af3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47af3-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47af3-143">INPUTS</span></span>

### <span data-ttu-id="47af3-144">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="47af3-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="47af3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="47af3-145">System.String</span></span>

## <span data-ttu-id="47af3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47af3-146">OUTPUTS</span></span>

### <span data-ttu-id="47af3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47af3-147">System.Boolean</span></span>

## <span data-ttu-id="47af3-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47af3-148">NOTES</span></span>

## <span data-ttu-id="47af3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47af3-149">RELATED LINKS</span></span>
