---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891204"
---
# <span data-ttu-id="3de95-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3de95-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="3de95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de95-102">SYNOPSIS</span></span>
<span data-ttu-id="3de95-103">Remove uma instância do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de95-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="3de95-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3de95-104">SYNTAX</span></span>

### <span data-ttu-id="3de95-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3de95-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de95-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de95-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de95-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de95-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de95-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3de95-108">DESCRIPTION</span></span>
<span data-ttu-id="3de95-109">O Remove-AzDataMigrationService cmdlet remove uma instância do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de95-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="3de95-110">O fornecimento do parâmetro DeleteRunningTask remove todas as tarefas do Serviço de Migração de Banco de Dados do Azure associadas ao serviço que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="3de95-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="3de95-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3de95-111">EXAMPLES</span></span>

### <span data-ttu-id="3de95-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3de95-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="3de95-113">O exemplo acima remove uma instância do Serviço de Migração de Banco de Dados do Azure chamado TestService que está contido em um Grupo de Recursos do Azure chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3de95-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="3de95-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3de95-114">PARAMETERS</span></span>

### <span data-ttu-id="3de95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de95-115">-DefaultProfile</span></span>
<span data-ttu-id="3de95-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3de95-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de95-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="3de95-117">-DeleteRunningTask</span></span>
<span data-ttu-id="3de95-118">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="3de95-118">Delete any running task</span></span>

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

### <span data-ttu-id="3de95-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3de95-119">-Force</span></span>
<span data-ttu-id="3de95-120">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="3de95-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3de95-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3de95-121">-InputObject</span></span>
<span data-ttu-id="3de95-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="3de95-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3de95-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3de95-123">-Name</span></span>
<span data-ttu-id="3de95-124">O nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="3de95-124">The name of the Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de95-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3de95-125">-PassThru</span></span>
<span data-ttu-id="3de95-126">Retorna um true/false.</span><span class="sxs-lookup"><span data-stu-id="3de95-126">Returns an true/false.</span></span>
<span data-ttu-id="3de95-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3de95-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3de95-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de95-128">-ResourceGroupName</span></span>
<span data-ttu-id="3de95-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de95-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3de95-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3de95-130">-ResourceId</span></span>
<span data-ttu-id="3de95-131">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="3de95-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="3de95-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3de95-132">-Confirm</span></span>
<span data-ttu-id="3de95-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de95-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de95-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de95-134">-WhatIf</span></span>
<span data-ttu-id="3de95-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3de95-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de95-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3de95-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de95-137">CommonParameters</span></span>
<span data-ttu-id="3de95-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de95-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de95-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de95-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3de95-140">INPUTS</span></span>

### <span data-ttu-id="3de95-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3de95-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3de95-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3de95-142">System.String</span></span>

## <span data-ttu-id="3de95-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3de95-143">OUTPUTS</span></span>

### <span data-ttu-id="3de95-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3de95-144">System.Boolean</span></span>

## <span data-ttu-id="3de95-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="3de95-145">NOTES</span></span>

## <span data-ttu-id="3de95-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3de95-146">RELATED LINKS</span></span>
