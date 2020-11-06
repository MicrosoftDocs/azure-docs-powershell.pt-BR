---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440465"
---
# <span data-ttu-id="04993-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="04993-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="04993-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04993-102">SYNOPSIS</span></span>
<span data-ttu-id="04993-103">Remove um projeto do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="04993-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04993-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04993-104">SYNTAX</span></span>

### <span data-ttu-id="04993-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="04993-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="04993-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04993-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="04993-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04993-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="04993-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04993-108">DESCRIPTION</span></span>
<span data-ttu-id="04993-109">O cmdlet Remove-AzureRmDataMigrationProject remove um projeto do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="04993-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="04993-110">Fornecer o parâmetro DeleteRunningTask remove todas as tarefas do serviço de migração do banco de dados do Azure associadas ao projeto que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="04993-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="04993-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04993-111">EXAMPLES</span></span>

### <span data-ttu-id="04993-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04993-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="04993-113">O exemplo acima remove o projeto do serviço de migração de banco de dados do Azure chamado myDMProject do Azure com base no nome como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="04993-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="04993-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="04993-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="04993-115">O exemplo acima remove o projeto do serviço de migração de banco de dados do Azure baseado no objeto PSProject como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="04993-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="04993-116">OS</span><span class="sxs-lookup"><span data-stu-id="04993-116">PARAMETERS</span></span>

### <span data-ttu-id="04993-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04993-117">-Confirm</span></span>
<span data-ttu-id="04993-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04993-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04993-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04993-119">-DefaultProfile</span></span>
<span data-ttu-id="04993-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04993-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04993-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="04993-121">-DeleteRunningTask</span></span>
<span data-ttu-id="04993-122">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="04993-122">Delete any running task</span></span>

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

### <span data-ttu-id="04993-123">-Force</span><span class="sxs-lookup"><span data-stu-id="04993-123">-Force</span></span>
<span data-ttu-id="04993-124">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="04993-124">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="04993-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04993-125">-InputObject</span></span>
<span data-ttu-id="04993-126">Objeto PSProject.</span><span class="sxs-lookup"><span data-stu-id="04993-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04993-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="04993-127">-Name</span></span>
<span data-ttu-id="04993-128">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="04993-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04993-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04993-129">-PassThru</span></span>
<span data-ttu-id="04993-130">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="04993-130">Returns an true/false.</span></span>
<span data-ttu-id="04993-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="04993-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04993-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04993-132">-ResourceGroupName</span></span>
<span data-ttu-id="04993-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04993-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="04993-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04993-134">-ResourceId</span></span>
<span data-ttu-id="04993-135">ID do recurso do projeto.</span><span class="sxs-lookup"><span data-stu-id="04993-135">Project Resource Id.</span></span>

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

### <span data-ttu-id="04993-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="04993-136">-ServiceName</span></span>
<span data-ttu-id="04993-137">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="04993-137">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="04993-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04993-138">-WhatIf</span></span>
<span data-ttu-id="04993-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04993-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04993-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04993-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="04993-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04993-141">INPUTS</span></span>

### <span data-ttu-id="04993-142">Microsoft. Azure. Commands. datamigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="04993-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="04993-143">System. String</span><span class="sxs-lookup"><span data-stu-id="04993-143">System.String</span></span>


## <span data-ttu-id="04993-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04993-144">OUTPUTS</span></span>

### <span data-ttu-id="04993-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04993-145">System.Boolean</span></span>


## <span data-ttu-id="04993-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04993-146">NOTES</span></span>

## <span data-ttu-id="04993-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04993-147">RELATED LINKS</span></span>

