---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: 7cf68cd27125580c6f0e57a7849c1fadc8cb47fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602863"
---
# <span data-ttu-id="4313b-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="4313b-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="4313b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4313b-102">SYNOPSIS</span></span>
<span data-ttu-id="4313b-103">Interrompe uma tarefa do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="4313b-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4313b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4313b-104">SYNTAX</span></span>

### <span data-ttu-id="4313b-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4313b-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4313b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4313b-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4313b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4313b-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4313b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4313b-108">DESCRIPTION</span></span>
<span data-ttu-id="4313b-109">Stop-AzureRmDataMigrationTask cmdlet interrompe a atividade de migração de banco de dados em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="4313b-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="4313b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4313b-110">EXAMPLES</span></span>

### <span data-ttu-id="4313b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4313b-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="4313b-112">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure chamada myDMSTask associada à instância do Project myDMSProject e do serviço de migração do banco de dados</span><span class="sxs-lookup"><span data-stu-id="4313b-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="4313b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4313b-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="4313b-114">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure passada como objeto PSProjectTask do parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="4313b-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="4313b-115">OS</span><span class="sxs-lookup"><span data-stu-id="4313b-115">PARAMETERS</span></span>

### <span data-ttu-id="4313b-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4313b-116">-Confirm</span></span>
<span data-ttu-id="4313b-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4313b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4313b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4313b-118">-DefaultProfile</span></span>
<span data-ttu-id="4313b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4313b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4313b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4313b-120">-InputObject</span></span>
<span data-ttu-id="4313b-121">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="4313b-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="4313b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4313b-122">-Name</span></span>
<span data-ttu-id="4313b-123">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4313b-123">The name of the task.</span></span>

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

### <span data-ttu-id="4313b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4313b-124">-PassThru</span></span>
<span data-ttu-id="4313b-125">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="4313b-125">Returns an true/false.</span></span>
<span data-ttu-id="4313b-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4313b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4313b-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4313b-127">-ProjectName</span></span>
<span data-ttu-id="4313b-128">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="4313b-128">The name of the project.</span></span>

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

### <span data-ttu-id="4313b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4313b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4313b-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4313b-130">The name of the resource group .</span></span>

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

### <span data-ttu-id="4313b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4313b-131">-ResourceId</span></span>
<span data-ttu-id="4313b-132">ProjectTask ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4313b-132">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="4313b-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4313b-133">-ServiceName</span></span>
<span data-ttu-id="4313b-134">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="4313b-134">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="4313b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4313b-135">-WhatIf</span></span>
<span data-ttu-id="4313b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4313b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4313b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4313b-137">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="4313b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4313b-138">INPUTS</span></span>

### <span data-ttu-id="4313b-139">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="4313b-139">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="4313b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4313b-140">System.String</span></span>


## <span data-ttu-id="4313b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4313b-141">OUTPUTS</span></span>

### <span data-ttu-id="4313b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4313b-142">System.Boolean</span></span>


## <span data-ttu-id="4313b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4313b-143">NOTES</span></span>

## <span data-ttu-id="4313b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4313b-144">RELATED LINKS</span></span>

