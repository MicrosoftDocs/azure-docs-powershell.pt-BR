---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: 9a6d2ba213054ea6b670205e84e3fd3893c59eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888706"
---
# <span data-ttu-id="8f60f-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8f60f-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="8f60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f60f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f60f-103">Interrompe uma instância do Serviço de Migração de Banco de Dados do Azure que está em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="8f60f-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8f60f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f60f-104">SYNTAX</span></span>

### <span data-ttu-id="8f60f-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f60f-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f60f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f60f-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f60f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f60f-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f60f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f60f-108">DESCRIPTION</span></span>
<span data-ttu-id="8f60f-109">O Stop-AzDataMigrationService cmdlet interrompe uma instância do Serviço de Migração de Banco de Dados do Azure que está em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="8f60f-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="8f60f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f60f-110">EXAMPLES</span></span>

### <span data-ttu-id="8f60f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f60f-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="8f60f-112">O exemplo acima interrompe uma instância do Serviço de Migração de Banco de Dados do Azure chamado TestService com base no nome do serviço passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="8f60f-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="8f60f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f60f-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="8f60f-114">O exemplo acima interrompe uma instância do Serviço de Migração de Banco de Dados do Azure com base no objeto PSDataMigrationService passado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="8f60f-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="8f60f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f60f-115">PARAMETERS</span></span>

### <span data-ttu-id="8f60f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f60f-116">-DefaultProfile</span></span>
<span data-ttu-id="8f60f-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8f60f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f60f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f60f-118">-InputObject</span></span>
<span data-ttu-id="8f60f-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8f60f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8f60f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f60f-120">-Name</span></span>
<span data-ttu-id="8f60f-121">Nome do Serviço de Migração de Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="8f60f-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="8f60f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f60f-122">-PassThru</span></span>
<span data-ttu-id="8f60f-123">Retorna um true/false.</span><span class="sxs-lookup"><span data-stu-id="8f60f-123">Returns an true/false.</span></span>
<span data-ttu-id="8f60f-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8f60f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f60f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f60f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f60f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f60f-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="8f60f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f60f-127">-ResourceId</span></span>
<span data-ttu-id="8f60f-128">ID do Recurso DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="8f60f-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8f60f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f60f-129">-Confirm</span></span>
<span data-ttu-id="8f60f-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f60f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f60f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f60f-131">-WhatIf</span></span>
<span data-ttu-id="8f60f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f60f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f60f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f60f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f60f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f60f-134">CommonParameters</span></span>
<span data-ttu-id="8f60f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f60f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f60f-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f60f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f60f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f60f-137">INPUTS</span></span>

### <span data-ttu-id="8f60f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8f60f-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="8f60f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8f60f-139">System.String</span></span>

## <span data-ttu-id="8f60f-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f60f-140">OUTPUTS</span></span>

### <span data-ttu-id="8f60f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f60f-141">System.Boolean</span></span>

## <span data-ttu-id="8f60f-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f60f-142">NOTES</span></span>

## <span data-ttu-id="8f60f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f60f-143">RELATED LINKS</span></span>
