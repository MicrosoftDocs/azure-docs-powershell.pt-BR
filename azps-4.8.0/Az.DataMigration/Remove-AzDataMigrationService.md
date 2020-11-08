---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 2ba182833fc1d4c59d9164b6db5d68bcd3c499f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112821"
---
# <span data-ttu-id="537cc-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="537cc-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="537cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="537cc-102">SYNOPSIS</span></span>
<span data-ttu-id="537cc-103">Remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="537cc-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="537cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="537cc-104">SYNTAX</span></span>

### <span data-ttu-id="537cc-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="537cc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="537cc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="537cc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="537cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="537cc-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="537cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="537cc-108">DESCRIPTION</span></span>
<span data-ttu-id="537cc-109">O cmdlet Remove-AzDataMigrationService remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="537cc-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="537cc-110">Fornecer o parâmetro DeleteRunningTask remove todas as tarefas do serviço de migração do banco de dados do Azure associadas ao serviço que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="537cc-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="537cc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="537cc-111">EXAMPLES</span></span>

### <span data-ttu-id="537cc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="537cc-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="537cc-113">O exemplo acima remove uma instância do serviço de migração de banco de dados do Azure chamado TestService que está contido em um grupo de recursos do Azure chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="537cc-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="537cc-114">OS</span><span class="sxs-lookup"><span data-stu-id="537cc-114">PARAMETERS</span></span>

### <span data-ttu-id="537cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537cc-115">-DefaultProfile</span></span>
<span data-ttu-id="537cc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="537cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="537cc-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="537cc-117">-DeleteRunningTask</span></span>
<span data-ttu-id="537cc-118">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="537cc-118">Delete any running task</span></span>

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

### <span data-ttu-id="537cc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="537cc-119">-Force</span></span>
<span data-ttu-id="537cc-120">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="537cc-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="537cc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="537cc-121">-InputObject</span></span>
<span data-ttu-id="537cc-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="537cc-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="537cc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="537cc-123">-Name</span></span>
<span data-ttu-id="537cc-124">O nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="537cc-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="537cc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="537cc-125">-PassThru</span></span>
<span data-ttu-id="537cc-126">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="537cc-126">Returns an true/false.</span></span>
<span data-ttu-id="537cc-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="537cc-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="537cc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="537cc-128">-ResourceGroupName</span></span>
<span data-ttu-id="537cc-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="537cc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="537cc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="537cc-130">-ResourceId</span></span>
<span data-ttu-id="537cc-131">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="537cc-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="537cc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="537cc-132">-Confirm</span></span>
<span data-ttu-id="537cc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="537cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="537cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="537cc-134">-WhatIf</span></span>
<span data-ttu-id="537cc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="537cc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="537cc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="537cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="537cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537cc-137">CommonParameters</span></span>
<span data-ttu-id="537cc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537cc-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="537cc-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537cc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="537cc-140">INPUTS</span></span>

### <span data-ttu-id="537cc-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="537cc-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="537cc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="537cc-142">System.String</span></span>

## <span data-ttu-id="537cc-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="537cc-143">OUTPUTS</span></span>

### <span data-ttu-id="537cc-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="537cc-144">System.Boolean</span></span>

## <span data-ttu-id="537cc-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="537cc-145">NOTES</span></span>

## <span data-ttu-id="537cc-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="537cc-146">RELATED LINKS</span></span>
