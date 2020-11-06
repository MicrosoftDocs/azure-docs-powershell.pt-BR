---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431683"
---
# <span data-ttu-id="fb225-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="fb225-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="fb225-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb225-102">SYNOPSIS</span></span>
<span data-ttu-id="fb225-103">Remove uma tarefa do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb225-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb225-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb225-104">SYNTAX</span></span>

### <span data-ttu-id="fb225-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb225-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fb225-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb225-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fb225-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb225-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fb225-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb225-108">DESCRIPTION</span></span>
<span data-ttu-id="fb225-109">O cmdlet Remove-AzureRmDataMigrationTask remove uma tarefa do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb225-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="fb225-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb225-110">EXAMPLES</span></span>

### <span data-ttu-id="fb225-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb225-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="fb225-112">O exemplo anterior remove uma tarefa do serviço de migração de banco de dados do Azure chamada Tarefateste do Azure com base no parâmetro nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fb225-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="fb225-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb225-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="fb225-114">O exemplo anterior remove uma tarefa do serviço de migração de banco de dados do Azure baseada no objeto PSProjectTask transmitido.</span><span class="sxs-lookup"><span data-stu-id="fb225-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="fb225-115">OS</span><span class="sxs-lookup"><span data-stu-id="fb225-115">PARAMETERS</span></span>

### <span data-ttu-id="fb225-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb225-116">-Confirm</span></span>
<span data-ttu-id="fb225-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb225-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb225-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb225-118">-DefaultProfile</span></span>
<span data-ttu-id="fb225-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb225-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb225-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fb225-120">-Force</span></span>
<span data-ttu-id="fb225-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="fb225-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fb225-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb225-122">-InputObject</span></span>
<span data-ttu-id="fb225-123">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="fb225-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb225-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb225-124">-Name</span></span>
<span data-ttu-id="fb225-125">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="fb225-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb225-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb225-126">-PassThru</span></span>
<span data-ttu-id="fb225-127">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="fb225-127">Returns an true/false.</span></span>
<span data-ttu-id="fb225-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fb225-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb225-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="fb225-129">-ProjectName</span></span>
<span data-ttu-id="fb225-130">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="fb225-130">The name of the project.</span></span>

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

### <span data-ttu-id="fb225-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb225-131">-ResourceGroupName</span></span>
<span data-ttu-id="fb225-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb225-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="fb225-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb225-133">-ResourceId</span></span>
<span data-ttu-id="fb225-134">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="fb225-134">Project Resource Id.</span></span>

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

### <span data-ttu-id="fb225-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fb225-135">-ServiceName</span></span>
<span data-ttu-id="fb225-136">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="fb225-136">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="fb225-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb225-137">-WhatIf</span></span>
<span data-ttu-id="fb225-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb225-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb225-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb225-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="fb225-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb225-140">INPUTS</span></span>

### <span data-ttu-id="fb225-141">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="fb225-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="fb225-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fb225-142">System.String</span></span>


## <span data-ttu-id="fb225-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb225-143">OUTPUTS</span></span>

### <span data-ttu-id="fb225-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb225-144">System.Boolean</span></span>


## <span data-ttu-id="fb225-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb225-145">NOTES</span></span>

## <span data-ttu-id="fb225-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb225-146">RELATED LINKS</span></span>


