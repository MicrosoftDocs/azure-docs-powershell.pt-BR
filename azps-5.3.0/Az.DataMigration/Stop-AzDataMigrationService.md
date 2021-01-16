---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271514"
---
# <span data-ttu-id="08ab8-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="08ab8-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="08ab8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="08ab8-103">Interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="08ab8-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="08ab8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08ab8-104">SYNTAX</span></span>

### <span data-ttu-id="08ab8-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="08ab8-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ab8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ab8-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08ab8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08ab8-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08ab8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08ab8-108">DESCRIPTION</span></span>
<span data-ttu-id="08ab8-109">O cmdlet Stop-AzDataMigrationService interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="08ab8-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="08ab8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08ab8-110">EXAMPLES</span></span>

### <span data-ttu-id="08ab8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08ab8-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="08ab8-112">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure chamado TestService com base no nome do serviço passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="08ab8-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="08ab8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="08ab8-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="08ab8-114">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure com base no objeto PSDataMigrationService passado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="08ab8-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="08ab8-115">OS</span><span class="sxs-lookup"><span data-stu-id="08ab8-115">PARAMETERS</span></span>

### <span data-ttu-id="08ab8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ab8-116">-DefaultProfile</span></span>
<span data-ttu-id="08ab8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08ab8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08ab8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08ab8-118">-InputObject</span></span>
<span data-ttu-id="08ab8-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="08ab8-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="08ab8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="08ab8-120">-Name</span></span>
<span data-ttu-id="08ab8-121">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="08ab8-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="08ab8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08ab8-122">-PassThru</span></span>
<span data-ttu-id="08ab8-123">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="08ab8-123">Returns an true/false.</span></span>
<span data-ttu-id="08ab8-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="08ab8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08ab8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ab8-125">-ResourceGroupName</span></span>
<span data-ttu-id="08ab8-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="08ab8-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="08ab8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08ab8-127">-ResourceId</span></span>
<span data-ttu-id="08ab8-128">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="08ab8-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="08ab8-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08ab8-129">-Confirm</span></span>
<span data-ttu-id="08ab8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08ab8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08ab8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08ab8-131">-WhatIf</span></span>
<span data-ttu-id="08ab8-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08ab8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08ab8-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08ab8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08ab8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ab8-134">CommonParameters</span></span>
<span data-ttu-id="08ab8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ab8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ab8-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ab8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ab8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08ab8-137">INPUTS</span></span>

### <span data-ttu-id="08ab8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="08ab8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="08ab8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="08ab8-139">System.String</span></span>

## <span data-ttu-id="08ab8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08ab8-140">OUTPUTS</span></span>

### <span data-ttu-id="08ab8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08ab8-141">System.Boolean</span></span>

## <span data-ttu-id="08ab8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08ab8-142">NOTES</span></span>

## <span data-ttu-id="08ab8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08ab8-143">RELATED LINKS</span></span>
