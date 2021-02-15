---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111929"
---
# <span data-ttu-id="3a6af-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3a6af-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="3a6af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a6af-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6af-103">Remove um projeto do Azure Database Migration Service do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6af-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="3a6af-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a6af-104">SYNTAX</span></span>

### <span data-ttu-id="3a6af-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a6af-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a6af-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a6af-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a6af-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a6af-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a6af-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a6af-108">DESCRIPTION</span></span>
<span data-ttu-id="3a6af-109">O Remove-AzDataMigrationProject cmdlet remove um projeto do Azure Database Migration Service do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6af-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="3a6af-110">O fornecimento do parâmetro DeleteRunningTask remove todas as tarefas do Serviço de Migração de Banco de Dados do Azure associadas ao projeto que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="3a6af-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="3a6af-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a6af-111">EXAMPLES</span></span>

### <span data-ttu-id="3a6af-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a6af-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="3a6af-113">O exemplo acima remove o projeto do Serviço de Migração de Banco de Dados do Azure chamado myDMProject do Azure com base no nome como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="3a6af-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="3a6af-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3a6af-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="3a6af-115">O exemplo acima remove o projeto do Serviço de Migração de Banco de Dados do Azure com base no objeto PSProject como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3a6af-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="3a6af-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a6af-116">PARAMETERS</span></span>

### <span data-ttu-id="3a6af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6af-117">-DefaultProfile</span></span>
<span data-ttu-id="3a6af-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3a6af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a6af-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="3a6af-119">-DeleteRunningTask</span></span>
<span data-ttu-id="3a6af-120">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="3a6af-120">Delete any running task</span></span>

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

### <span data-ttu-id="3a6af-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3a6af-121">-Force</span></span>
<span data-ttu-id="3a6af-122">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="3a6af-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3a6af-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a6af-123">-InputObject</span></span>
<span data-ttu-id="3a6af-124">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="3a6af-124">PSProject Object.</span></span>

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

### <span data-ttu-id="3a6af-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a6af-125">-Name</span></span>
<span data-ttu-id="3a6af-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="3a6af-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6af-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a6af-127">-PassThru</span></span>
<span data-ttu-id="3a6af-128">Retorna um verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="3a6af-128">Returns an true/false.</span></span>
<span data-ttu-id="3a6af-129">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="3a6af-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a6af-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6af-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a6af-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a6af-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a6af-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a6af-132">-ResourceId</span></span>
<span data-ttu-id="3a6af-133">ID do Recurso do Projeto.</span><span class="sxs-lookup"><span data-stu-id="3a6af-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="3a6af-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3a6af-134">-ServiceName</span></span>
<span data-ttu-id="3a6af-135">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a6af-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="3a6af-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3a6af-136">-Confirm</span></span>
<span data-ttu-id="3a6af-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6af-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6af-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6af-138">-WhatIf</span></span>
<span data-ttu-id="3a6af-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3a6af-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6af-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a6af-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6af-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6af-141">CommonParameters</span></span>
<span data-ttu-id="3a6af-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6af-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6af-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6af-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6af-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="3a6af-144">INPUTS</span></span>

### <span data-ttu-id="3a6af-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="3a6af-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="3a6af-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3a6af-146">System.String</span></span>

## <span data-ttu-id="3a6af-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="3a6af-147">OUTPUTS</span></span>

### <span data-ttu-id="3a6af-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a6af-148">System.Boolean</span></span>

## <span data-ttu-id="3a6af-149">Notas</span><span class="sxs-lookup"><span data-stu-id="3a6af-149">NOTES</span></span>

## <span data-ttu-id="3a6af-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a6af-150">RELATED LINKS</span></span>
