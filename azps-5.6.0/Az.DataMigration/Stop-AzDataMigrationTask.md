---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 33bc407c5585017bfe98591649a0c30e46adfea4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885878"
---
# <span data-ttu-id="14e23-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="14e23-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="14e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e23-102">SYNOPSIS</span></span>
<span data-ttu-id="14e23-103">Interrompe uma tarefa do Serviço de Migração de Banco de Dados do Azure que está em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="14e23-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="14e23-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14e23-104">SYNTAX</span></span>

### <span data-ttu-id="14e23-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="14e23-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14e23-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14e23-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14e23-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14e23-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14e23-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14e23-108">DESCRIPTION</span></span>
<span data-ttu-id="14e23-109">Stop-AzDataMigrationTask cmdlet interrompe a atividade de migração de banco de dados em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="14e23-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="14e23-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14e23-110">EXAMPLES</span></span>

### <span data-ttu-id="14e23-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14e23-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="14e23-112">Exemplo acima interrompe a tarefa do Serviço de Migração de Banco de Dados do Azure chamada myDMSTask associada ao projeto myDMSProject e à instância do Serviço de Migração de Banco de Dados do Azure chamada TestService</span><span class="sxs-lookup"><span data-stu-id="14e23-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="14e23-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="14e23-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="14e23-114">Exemplo acima interrompe a tarefa do Serviço de Migração de Banco de Dados do Azure passada como objeto PSProjectTask do parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="14e23-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="14e23-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14e23-115">PARAMETERS</span></span>

### <span data-ttu-id="14e23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e23-116">-DefaultProfile</span></span>
<span data-ttu-id="14e23-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="14e23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14e23-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e23-118">-InputObject</span></span>
<span data-ttu-id="14e23-119">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="14e23-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="14e23-120">-Name</span><span class="sxs-lookup"><span data-stu-id="14e23-120">-Name</span></span>
<span data-ttu-id="14e23-121">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="14e23-121">The name of the task.</span></span>

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

### <span data-ttu-id="14e23-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14e23-122">-PassThru</span></span>
<span data-ttu-id="14e23-123">Retorna um true/false.</span><span class="sxs-lookup"><span data-stu-id="14e23-123">Returns an true/false.</span></span>
<span data-ttu-id="14e23-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="14e23-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14e23-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="14e23-125">-ProjectName</span></span>
<span data-ttu-id="14e23-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="14e23-126">The name of the project.</span></span>

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

### <span data-ttu-id="14e23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e23-127">-ResourceGroupName</span></span>
<span data-ttu-id="14e23-128">O nome do grupo de recursos .</span><span class="sxs-lookup"><span data-stu-id="14e23-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="14e23-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14e23-129">-ResourceId</span></span>
<span data-ttu-id="14e23-130">ID do Recurso ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="14e23-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="14e23-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="14e23-131">-ServiceName</span></span>
<span data-ttu-id="14e23-132">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="14e23-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="14e23-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e23-133">-Confirm</span></span>
<span data-ttu-id="14e23-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14e23-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e23-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14e23-135">-WhatIf</span></span>
<span data-ttu-id="14e23-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14e23-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e23-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14e23-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e23-138">CommonParameters</span></span>
<span data-ttu-id="14e23-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e23-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e23-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e23-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14e23-141">INPUTS</span></span>

### <span data-ttu-id="14e23-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="14e23-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="14e23-143">System.String</span><span class="sxs-lookup"><span data-stu-id="14e23-143">System.String</span></span>

## <span data-ttu-id="14e23-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14e23-144">OUTPUTS</span></span>

### <span data-ttu-id="14e23-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14e23-145">System.Boolean</span></span>

## <span data-ttu-id="14e23-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="14e23-146">NOTES</span></span>

## <span data-ttu-id="14e23-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14e23-147">RELATED LINKS</span></span>
