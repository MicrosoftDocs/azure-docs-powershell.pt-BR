---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111928"
---
# <span data-ttu-id="2b041-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2b041-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="2b041-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b041-102">SYNOPSIS</span></span>
<span data-ttu-id="2b041-103">Remove uma instância do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b041-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="2b041-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b041-104">SYNTAX</span></span>

### <span data-ttu-id="2b041-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b041-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b041-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b041-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b041-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b041-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b041-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b041-108">DESCRIPTION</span></span>
<span data-ttu-id="2b041-109">O Remove-AzDataMigrationService cmdlet remove uma instância do Serviço de Migração de Banco de Dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b041-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="2b041-110">O fornecimento do parâmetro DeleteRunningTask remove todas as tarefas do Serviço de Migração de Banco de Dados do Azure associadas ao serviço que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="2b041-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="2b041-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2b041-111">EXAMPLES</span></span>

### <span data-ttu-id="2b041-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b041-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="2b041-113">O exemplo acima remove uma instância do Serviço de Migração de Banco de Dados do Azure chamada TestService que está contida em um Grupo de Recursos do Azure chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b041-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="2b041-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b041-114">PARAMETERS</span></span>

### <span data-ttu-id="2b041-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b041-115">-DefaultProfile</span></span>
<span data-ttu-id="2b041-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2b041-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b041-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="2b041-117">-DeleteRunningTask</span></span>
<span data-ttu-id="2b041-118">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="2b041-118">Delete any running task</span></span>

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

### <span data-ttu-id="2b041-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2b041-119">-Force</span></span>
<span data-ttu-id="2b041-120">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="2b041-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2b041-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b041-121">-InputObject</span></span>
<span data-ttu-id="2b041-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2b041-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="2b041-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b041-123">-Name</span></span>
<span data-ttu-id="2b041-124">O nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="2b041-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="2b041-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b041-125">-PassThru</span></span>
<span data-ttu-id="2b041-126">Retorna um verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="2b041-126">Returns an true/false.</span></span>
<span data-ttu-id="2b041-127">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="2b041-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b041-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b041-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b041-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b041-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b041-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b041-130">-ResourceId</span></span>
<span data-ttu-id="2b041-131">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="2b041-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="2b041-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2b041-132">-Confirm</span></span>
<span data-ttu-id="2b041-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b041-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b041-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b041-134">-WhatIf</span></span>
<span data-ttu-id="2b041-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2b041-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b041-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b041-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b041-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b041-137">CommonParameters</span></span>
<span data-ttu-id="2b041-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b041-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b041-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b041-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b041-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="2b041-140">INPUTS</span></span>

### <span data-ttu-id="2b041-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2b041-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="2b041-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2b041-142">System.String</span></span>

## <span data-ttu-id="2b041-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="2b041-143">OUTPUTS</span></span>

### <span data-ttu-id="2b041-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b041-144">System.Boolean</span></span>

## <span data-ttu-id="2b041-145">Notas</span><span class="sxs-lookup"><span data-stu-id="2b041-145">NOTES</span></span>

## <span data-ttu-id="2b041-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b041-146">RELATED LINKS</span></span>
