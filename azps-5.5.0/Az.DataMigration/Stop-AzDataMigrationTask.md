---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116237"
---
# <span data-ttu-id="158fe-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="158fe-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="158fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="158fe-102">SYNOPSIS</span></span>
<span data-ttu-id="158fe-103">Interrompe uma tarefa do Serviço de Migração de Banco de Dados do Azure que está em execução.</span><span class="sxs-lookup"><span data-stu-id="158fe-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="158fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="158fe-104">SYNTAX</span></span>

### <span data-ttu-id="158fe-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="158fe-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="158fe-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="158fe-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="158fe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="158fe-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="158fe-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="158fe-108">DESCRIPTION</span></span>
<span data-ttu-id="158fe-109">Stop-AzDataMigrationTask cmdlet interrompe a atividade de migração de banco de dados em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="158fe-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="158fe-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="158fe-110">EXAMPLES</span></span>

### <span data-ttu-id="158fe-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="158fe-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="158fe-112">Exemplo acima interrompe a tarefa do Serviço de Migração de Banco de Dados do Azure chamada myDMSTask associada ao project myDMSProject e à instância do Serviço de Migração de Banco de Dados do Azure chamada TestService</span><span class="sxs-lookup"><span data-stu-id="158fe-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="158fe-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="158fe-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="158fe-114">Exemplo acima interrompe a tarefa do Serviço de Migração de Banco de Dados do Azure passada como objeto PSProjectTask do parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="158fe-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="158fe-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="158fe-115">PARAMETERS</span></span>

### <span data-ttu-id="158fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158fe-116">-DefaultProfile</span></span>
<span data-ttu-id="158fe-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="158fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="158fe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="158fe-118">-InputObject</span></span>
<span data-ttu-id="158fe-119">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="158fe-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="158fe-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="158fe-120">-Name</span></span>
<span data-ttu-id="158fe-121">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="158fe-121">The name of the task.</span></span>

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

### <span data-ttu-id="158fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="158fe-122">-PassThru</span></span>
<span data-ttu-id="158fe-123">Retorna um verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="158fe-123">Returns an true/false.</span></span>
<span data-ttu-id="158fe-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="158fe-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="158fe-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="158fe-125">-ProjectName</span></span>
<span data-ttu-id="158fe-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="158fe-126">The name of the project.</span></span>

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

### <span data-ttu-id="158fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="158fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="158fe-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="158fe-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="158fe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="158fe-129">-ResourceId</span></span>
<span data-ttu-id="158fe-130">ID do Recurso ProjectTask.</span><span class="sxs-lookup"><span data-stu-id="158fe-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="158fe-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="158fe-131">-ServiceName</span></span>
<span data-ttu-id="158fe-132">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="158fe-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="158fe-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="158fe-133">-Confirm</span></span>
<span data-ttu-id="158fe-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="158fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="158fe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158fe-135">-WhatIf</span></span>
<span data-ttu-id="158fe-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="158fe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="158fe-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="158fe-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="158fe-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158fe-138">CommonParameters</span></span>
<span data-ttu-id="158fe-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158fe-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158fe-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158fe-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158fe-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="158fe-141">INPUTS</span></span>

### <span data-ttu-id="158fe-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="158fe-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="158fe-143">System.String</span><span class="sxs-lookup"><span data-stu-id="158fe-143">System.String</span></span>

## <span data-ttu-id="158fe-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="158fe-144">OUTPUTS</span></span>

### <span data-ttu-id="158fe-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="158fe-145">System.Boolean</span></span>

## <span data-ttu-id="158fe-146">Notas</span><span class="sxs-lookup"><span data-stu-id="158fe-146">NOTES</span></span>

## <span data-ttu-id="158fe-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="158fe-147">RELATED LINKS</span></span>
