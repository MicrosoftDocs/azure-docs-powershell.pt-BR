---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432133"
---
# <span data-ttu-id="f5326-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f5326-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="f5326-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5326-102">SYNOPSIS</span></span>
<span data-ttu-id="f5326-103">Remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5326-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5326-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5326-104">SYNTAX</span></span>

### <span data-ttu-id="f5326-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5326-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5326-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5326-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f5326-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5326-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f5326-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5326-108">DESCRIPTION</span></span>
<span data-ttu-id="f5326-109">O cmdlet Remove-AzureRmDataMigrationService remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5326-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="f5326-110">Fornecer o parâmetro DeleteRunningTask remove todas as tarefas do serviço de migração do banco de dados do Azure associadas ao serviço que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="f5326-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="f5326-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5326-111">EXAMPLES</span></span>

### <span data-ttu-id="f5326-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5326-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="f5326-113">O exemplo acima remove uma instância do serviço de migração de banco de dados do Azure chamado TestService que está contido em um grupo de recursos do Azure chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="f5326-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="f5326-114">OS</span><span class="sxs-lookup"><span data-stu-id="f5326-114">PARAMETERS</span></span>

### <span data-ttu-id="f5326-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5326-115">-Confirm</span></span>
<span data-ttu-id="f5326-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5326-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5326-117">-DefaultProfile</span></span>
<span data-ttu-id="f5326-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5326-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="f5326-119">-DeleteRunningTask</span></span>
<span data-ttu-id="f5326-120">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="f5326-120">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f5326-121">-Force</span></span>
<span data-ttu-id="f5326-122">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f5326-122">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5326-123">-InputObject</span></span>
<span data-ttu-id="f5326-124">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f5326-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5326-125">-Name</span></span>
<span data-ttu-id="f5326-126">O nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="f5326-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5326-127">-PassThru</span></span>
<span data-ttu-id="f5326-128">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="f5326-128">Returns an true/false.</span></span>
<span data-ttu-id="f5326-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f5326-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5326-130">-ResourceGroupName</span></span>
<span data-ttu-id="f5326-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5326-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5326-132">-ResourceId</span></span>
<span data-ttu-id="f5326-133">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f5326-133">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5326-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5326-134">-WhatIf</span></span>
<span data-ttu-id="f5326-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5326-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5326-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5326-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f5326-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5326-137">INPUTS</span></span>

### <span data-ttu-id="f5326-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f5326-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="f5326-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5326-139">System.String</span></span>


## <span data-ttu-id="f5326-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5326-140">OUTPUTS</span></span>

### <span data-ttu-id="f5326-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5326-141">System.Boolean</span></span>


## <span data-ttu-id="f5326-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5326-142">NOTES</span></span>

## <span data-ttu-id="f5326-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5326-143">RELATED LINKS</span></span>


