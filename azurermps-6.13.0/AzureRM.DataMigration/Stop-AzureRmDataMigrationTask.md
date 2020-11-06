---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationTask.md
ms.openlocfilehash: aec7870522d5d25887c9cb7437a4a232d3021a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431966"
---
# <span data-ttu-id="9c188-101">Stop-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="9c188-101">Stop-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="9c188-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c188-102">SYNOPSIS</span></span>
<span data-ttu-id="9c188-103">Interrompe uma tarefa do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="9c188-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c188-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c188-104">SYNTAX</span></span>

### <span data-ttu-id="9c188-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c188-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c188-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c188-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c188-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c188-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c188-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c188-108">DESCRIPTION</span></span>
<span data-ttu-id="9c188-109">Stop-AzureRmDataMigrationTask cmdlet interrompe a atividade de migração de banco de dados em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="9c188-109">Stop-AzureRmDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="9c188-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c188-110">EXAMPLES</span></span>

### <span data-ttu-id="9c188-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c188-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="9c188-112">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure chamada myDMSTask associada à instância do Project myDMSProject e do serviço de migração do banco de dados</span><span class="sxs-lookup"><span data-stu-id="9c188-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="9c188-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c188-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="9c188-114">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure passada como objeto PSProjectTask do parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="9c188-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="9c188-115">OS</span><span class="sxs-lookup"><span data-stu-id="9c188-115">PARAMETERS</span></span>

### <span data-ttu-id="9c188-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c188-116">-DefaultProfile</span></span>
<span data-ttu-id="9c188-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c188-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c188-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c188-118">-InputObject</span></span>
<span data-ttu-id="9c188-119">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="9c188-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c188-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c188-120">-Name</span></span>
<span data-ttu-id="9c188-121">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9c188-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c188-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c188-122">-PassThru</span></span>
<span data-ttu-id="9c188-123">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="9c188-123">Returns an true/false.</span></span>
<span data-ttu-id="9c188-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9c188-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c188-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="9c188-125">-ProjectName</span></span>
<span data-ttu-id="9c188-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c188-126">The name of the project.</span></span>

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

### <span data-ttu-id="9c188-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c188-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c188-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c188-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="9c188-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c188-129">-ResourceId</span></span>
<span data-ttu-id="9c188-130">ProjectTask ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c188-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="9c188-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9c188-131">-ServiceName</span></span>
<span data-ttu-id="9c188-132">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9c188-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="9c188-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c188-133">-Confirm</span></span>
<span data-ttu-id="9c188-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c188-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c188-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c188-135">-WhatIf</span></span>
<span data-ttu-id="9c188-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c188-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c188-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c188-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c188-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c188-138">CommonParameters</span></span>
<span data-ttu-id="9c188-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c188-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c188-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c188-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c188-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c188-141">INPUTS</span></span>

### <span data-ttu-id="9c188-142">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="9c188-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="9c188-143">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c188-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9c188-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9c188-144">System.String</span></span>

## <span data-ttu-id="9c188-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c188-145">OUTPUTS</span></span>

### <span data-ttu-id="9c188-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c188-146">System.Boolean</span></span>

## <span data-ttu-id="9c188-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c188-147">NOTES</span></span>

## <span data-ttu-id="9c188-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c188-148">RELATED LINKS</span></span>
