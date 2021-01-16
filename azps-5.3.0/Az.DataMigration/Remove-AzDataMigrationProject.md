---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: f45134cae9c77108aca4084470fd7f919fde02a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271524"
---
# <span data-ttu-id="9caa0-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="9caa0-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="9caa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9caa0-102">SYNOPSIS</span></span>
<span data-ttu-id="9caa0-103">Remove um projeto do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="9caa0-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="9caa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9caa0-104">SYNTAX</span></span>

### <span data-ttu-id="9caa0-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9caa0-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9caa0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9caa0-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9caa0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9caa0-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9caa0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9caa0-108">DESCRIPTION</span></span>
<span data-ttu-id="9caa0-109">O cmdlet Remove-AzDataMigrationProject remove um projeto do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="9caa0-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="9caa0-110">Fornecer o parâmetro DeleteRunningTask remove todas as tarefas do serviço de migração do banco de dados do Azure associadas ao projeto que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="9caa0-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="9caa0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9caa0-111">EXAMPLES</span></span>

### <span data-ttu-id="9caa0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9caa0-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="9caa0-113">O exemplo acima remove o projeto do serviço de migração de banco de dados do Azure chamado myDMProject do Azure com base no nome como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="9caa0-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="9caa0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9caa0-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="9caa0-115">O exemplo acima remove o projeto do serviço de migração de banco de dados do Azure baseado no objeto PSProject como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="9caa0-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="9caa0-116">OS</span><span class="sxs-lookup"><span data-stu-id="9caa0-116">PARAMETERS</span></span>

### <span data-ttu-id="9caa0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9caa0-117">-DefaultProfile</span></span>
<span data-ttu-id="9caa0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9caa0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9caa0-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="9caa0-119">-DeleteRunningTask</span></span>
<span data-ttu-id="9caa0-120">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="9caa0-120">Delete any running task</span></span>

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

### <span data-ttu-id="9caa0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9caa0-121">-Force</span></span>
<span data-ttu-id="9caa0-122">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="9caa0-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9caa0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9caa0-123">-InputObject</span></span>
<span data-ttu-id="9caa0-124">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="9caa0-124">PSProject Object.</span></span>

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

### <span data-ttu-id="9caa0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9caa0-125">-Name</span></span>
<span data-ttu-id="9caa0-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="9caa0-126">The name of the project.</span></span>

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

### <span data-ttu-id="9caa0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9caa0-127">-PassThru</span></span>
<span data-ttu-id="9caa0-128">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="9caa0-128">Returns an true/false.</span></span>
<span data-ttu-id="9caa0-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9caa0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9caa0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9caa0-130">-ResourceGroupName</span></span>
<span data-ttu-id="9caa0-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9caa0-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="9caa0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9caa0-132">-ResourceId</span></span>
<span data-ttu-id="9caa0-133">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="9caa0-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="9caa0-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9caa0-134">-ServiceName</span></span>
<span data-ttu-id="9caa0-135">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9caa0-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9caa0-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9caa0-136">-Confirm</span></span>
<span data-ttu-id="9caa0-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9caa0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9caa0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9caa0-138">-WhatIf</span></span>
<span data-ttu-id="9caa0-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9caa0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9caa0-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9caa0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9caa0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9caa0-141">CommonParameters</span></span>
<span data-ttu-id="9caa0-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9caa0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9caa0-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9caa0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9caa0-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9caa0-144">INPUTS</span></span>

### <span data-ttu-id="9caa0-145">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="9caa0-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="9caa0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9caa0-146">System.String</span></span>

## <span data-ttu-id="9caa0-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9caa0-147">OUTPUTS</span></span>

### <span data-ttu-id="9caa0-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9caa0-148">System.Boolean</span></span>

## <span data-ttu-id="9caa0-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9caa0-149">NOTES</span></span>

## <span data-ttu-id="9caa0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9caa0-150">RELATED LINKS</span></span>
