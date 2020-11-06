---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: 677e89dd0def314744e507c6e61c745f39a081bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440054"
---
# <span data-ttu-id="cb33f-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cb33f-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="cb33f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb33f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb33f-103">Remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb33f-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb33f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb33f-104">SYNTAX</span></span>

### <span data-ttu-id="cb33f-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cb33f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb33f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb33f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb33f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb33f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb33f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb33f-108">DESCRIPTION</span></span>
<span data-ttu-id="cb33f-109">O cmdlet Remove-AzureRmDataMigrationService remove uma instância do serviço de migração de banco de dados do Azure do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb33f-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="cb33f-110">Fornecer o parâmetro DeleteRunningTask remove todas as tarefas do serviço de migração do banco de dados do Azure associadas ao serviço que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="cb33f-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="cb33f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb33f-111">EXAMPLES</span></span>

### <span data-ttu-id="cb33f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb33f-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="cb33f-113">O exemplo acima remove uma instância do serviço de migração de banco de dados do Azure chamado TestService que está contido em um grupo de recursos do Azure chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="cb33f-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="cb33f-114">OS</span><span class="sxs-lookup"><span data-stu-id="cb33f-114">PARAMETERS</span></span>

### <span data-ttu-id="cb33f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb33f-115">-DefaultProfile</span></span>
<span data-ttu-id="cb33f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb33f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb33f-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="cb33f-117">-DeleteRunningTask</span></span>
<span data-ttu-id="cb33f-118">Excluir qualquer tarefa em execução</span><span class="sxs-lookup"><span data-stu-id="cb33f-118">Delete any running task</span></span>

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

### <span data-ttu-id="cb33f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cb33f-119">-Force</span></span>
<span data-ttu-id="cb33f-120">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="cb33f-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cb33f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb33f-121">-InputObject</span></span>
<span data-ttu-id="cb33f-122">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="cb33f-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="cb33f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb33f-123">-Name</span></span>
<span data-ttu-id="cb33f-124">O nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cb33f-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="cb33f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb33f-125">-PassThru</span></span>
<span data-ttu-id="cb33f-126">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="cb33f-126">Returns an true/false.</span></span>
<span data-ttu-id="cb33f-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cb33f-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb33f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb33f-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb33f-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb33f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb33f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb33f-130">-ResourceId</span></span>
<span data-ttu-id="cb33f-131">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cb33f-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="cb33f-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb33f-132">-Confirm</span></span>
<span data-ttu-id="cb33f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb33f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb33f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb33f-134">-WhatIf</span></span>
<span data-ttu-id="cb33f-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb33f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb33f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb33f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb33f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb33f-137">CommonParameters</span></span>
<span data-ttu-id="cb33f-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb33f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb33f-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb33f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb33f-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb33f-140">INPUTS</span></span>

### <span data-ttu-id="cb33f-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cb33f-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="cb33f-142">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb33f-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cb33f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="cb33f-143">System.String</span></span>

## <span data-ttu-id="cb33f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb33f-144">OUTPUTS</span></span>

### <span data-ttu-id="cb33f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb33f-145">System.Boolean</span></span>

## <span data-ttu-id="cb33f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb33f-146">NOTES</span></span>

## <span data-ttu-id="cb33f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb33f-147">RELATED LINKS</span></span>
