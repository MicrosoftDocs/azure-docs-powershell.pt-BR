---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: c7e27deb3a625d88cb2b84bfa1b53fb28ca553ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257648"
---
# <span data-ttu-id="a663c-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a663c-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="a663c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a663c-102">SYNOPSIS</span></span>
<span data-ttu-id="a663c-103">Interrompe uma tarefa do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="a663c-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="a663c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a663c-104">SYNTAX</span></span>

### <span data-ttu-id="a663c-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a663c-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a663c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a663c-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a663c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a663c-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a663c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a663c-108">DESCRIPTION</span></span>
<span data-ttu-id="a663c-109">Stop-AzDataMigrationTask cmdlet interrompe a atividade de migração de banco de dados em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="a663c-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="a663c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a663c-110">EXAMPLES</span></span>

### <span data-ttu-id="a663c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a663c-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="a663c-112">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure chamada myDMSTask associada à instância do Project myDMSProject e do serviço de migração do banco de dados</span><span class="sxs-lookup"><span data-stu-id="a663c-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="a663c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a663c-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="a663c-114">O exemplo acima interrompe a tarefa do serviço de migração de banco de dados do Azure passada como objeto PSProjectTask do parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="a663c-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="a663c-115">OS</span><span class="sxs-lookup"><span data-stu-id="a663c-115">PARAMETERS</span></span>

### <span data-ttu-id="a663c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a663c-116">-DefaultProfile</span></span>
<span data-ttu-id="a663c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a663c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a663c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a663c-118">-InputObject</span></span>
<span data-ttu-id="a663c-119">Objeto PSProjectTask.</span><span class="sxs-lookup"><span data-stu-id="a663c-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="a663c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a663c-120">-Name</span></span>
<span data-ttu-id="a663c-121">O nome da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a663c-121">The name of the task.</span></span>

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

### <span data-ttu-id="a663c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a663c-122">-PassThru</span></span>
<span data-ttu-id="a663c-123">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="a663c-123">Returns an true/false.</span></span>
<span data-ttu-id="a663c-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a663c-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a663c-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a663c-125">-ProjectName</span></span>
<span data-ttu-id="a663c-126">O nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="a663c-126">The name of the project.</span></span>

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

### <span data-ttu-id="a663c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a663c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a663c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a663c-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="a663c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a663c-129">-ResourceId</span></span>
<span data-ttu-id="a663c-130">ProjectTask ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a663c-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="a663c-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a663c-131">-ServiceName</span></span>
<span data-ttu-id="a663c-132">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a663c-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="a663c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a663c-133">-Confirm</span></span>
<span data-ttu-id="a663c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a663c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a663c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a663c-135">-WhatIf</span></span>
<span data-ttu-id="a663c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a663c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a663c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a663c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a663c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a663c-138">CommonParameters</span></span>
<span data-ttu-id="a663c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a663c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a663c-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a663c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a663c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a663c-141">INPUTS</span></span>

### <span data-ttu-id="a663c-142">Microsoft. Azure. Commands. datamigration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="a663c-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="a663c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a663c-143">System.String</span></span>

## <span data-ttu-id="a663c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a663c-144">OUTPUTS</span></span>

### <span data-ttu-id="a663c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a663c-145">System.Boolean</span></span>

## <span data-ttu-id="a663c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a663c-146">NOTES</span></span>

## <span data-ttu-id="a663c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a663c-147">RELATED LINKS</span></span>
