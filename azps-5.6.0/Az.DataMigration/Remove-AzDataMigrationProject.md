---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 449a1cfc3156b647eccee6fc320f41fa9e53549c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892978"
---
# <span data-ttu-id="8b2f3-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="8b2f3-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="8b2f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2f3-103">Remove um projeto do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="8b2f3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8b2f3-104">SYNTAX</span></span>

### <span data-ttu-id="8b2f3-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8b2f3-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b2f3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b2f3-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b2f3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b2f3-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b2f3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8b2f3-108">DESCRIPTION</span></span>
<span data-ttu-id="8b2f3-109">O Remove-AzDataMigrationProject cmdlet remove um projeto do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="8b2f3-110">O fornecimento do parâmetro DeleteRunningTask remove todas as tarefas do Serviço de Migração de Banco de Dados do Azure associadas ao projeto que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="8b2f3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-111">EXAMPLES</span></span>

### <span data-ttu-id="8b2f3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b2f3-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="8b2f3-113">O exemplo acima remove o projeto do Serviço de Migração de Banco de Dados do Azure chamado myDMProject do Azure com base no nome como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="8b2f3-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="8b2f3-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8b2f3-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="8b2f3-115">O exemplo acima remove o projeto do Serviço de Migração de Banco de Dados do Azure com base no objeto PSProject como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="8b2f3-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-116">PARAMETERS</span></span>

### <span data-ttu-id="8b2f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2f3-117">-DefaultProfile</span></span>
<span data-ttu-id="8b2f3-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b2f3-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="8b2f3-119">-DeleteRunningTask</span></span>
<span data-ttu-id="8b2f3-120">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="8b2f3-120">Delete any running task</span></span>

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

### <span data-ttu-id="8b2f3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8b2f3-121">-Force</span></span>
<span data-ttu-id="8b2f3-122">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="8b2f3-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8b2f3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b2f3-123">-InputObject</span></span>
<span data-ttu-id="8b2f3-124">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-124">PSProject Object.</span></span>

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

### <span data-ttu-id="8b2f3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8b2f3-125">-Name</span></span>
<span data-ttu-id="8b2f3-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-126">The name of the project.</span></span>

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

### <span data-ttu-id="8b2f3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b2f3-127">-PassThru</span></span>
<span data-ttu-id="8b2f3-128">Retorna um true/false.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-128">Returns an true/false.</span></span>
<span data-ttu-id="8b2f3-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b2f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="8b2f3-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="8b2f3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b2f3-132">-ResourceId</span></span>
<span data-ttu-id="8b2f3-133">ID do Recurso do Project.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="8b2f3-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8b2f3-134">-ServiceName</span></span>
<span data-ttu-id="8b2f3-135">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8b2f3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b2f3-136">-Confirm</span></span>
<span data-ttu-id="8b2f3-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2f3-138">-WhatIf</span></span>
<span data-ttu-id="8b2f3-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2f3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2f3-141">CommonParameters</span></span>
<span data-ttu-id="8b2f3-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2f3-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b2f3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2f3-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-144">INPUTS</span></span>

### <span data-ttu-id="8b2f3-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="8b2f3-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="8b2f3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8b2f3-146">System.String</span></span>

## <span data-ttu-id="8b2f3-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-147">OUTPUTS</span></span>

### <span data-ttu-id="8b2f3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b2f3-148">System.Boolean</span></span>

## <span data-ttu-id="8b2f3-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="8b2f3-149">NOTES</span></span>

## <span data-ttu-id="8b2f3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b2f3-150">RELATED LINKS</span></span>
