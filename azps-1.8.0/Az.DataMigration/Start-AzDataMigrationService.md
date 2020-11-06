---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 67194bfc9a7ce1971817c7f80e7a5ee61caf6db0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601022"
---
# <span data-ttu-id="85832-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="85832-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="85832-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85832-102">SYNOPSIS</span></span>
<span data-ttu-id="85832-103">Inicia uma instância do serviço de migração do banco de dados do Azure em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="85832-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="85832-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85832-104">SYNTAX</span></span>

### <span data-ttu-id="85832-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85832-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85832-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85832-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85832-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85832-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85832-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85832-108">DESCRIPTION</span></span>
<span data-ttu-id="85832-109">O cmdlet Start-AzDataMigrationService inicia uma instância do serviço de migração do banco de dados do Azure em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="85832-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="85832-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85832-110">EXAMPLES</span></span>

### <span data-ttu-id="85832-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85832-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="85832-112">O exemplo acima inicia uma instância do serviço de migração de banco de dados do Azure chamada serviço de teste em um estado parado com base no nome do serviço passado como entrada</span><span class="sxs-lookup"><span data-stu-id="85832-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="85832-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="85832-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="85832-114">O exemplo acima inicia uma instância do serviço de migração do banco de dados do Azure com base no PSDataMigrationService passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="85832-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="85832-115">OS</span><span class="sxs-lookup"><span data-stu-id="85832-115">PARAMETERS</span></span>

### <span data-ttu-id="85832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85832-116">-DefaultProfile</span></span>
<span data-ttu-id="85832-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85832-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85832-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85832-118">-InputObject</span></span>
<span data-ttu-id="85832-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="85832-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="85832-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="85832-120">-Name</span></span>
<span data-ttu-id="85832-121">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="85832-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="85832-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85832-122">-PassThru</span></span>
<span data-ttu-id="85832-123">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="85832-123">Returns an true/false.</span></span>
<span data-ttu-id="85832-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="85832-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85832-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85832-125">-ResourceGroupName</span></span>
<span data-ttu-id="85832-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85832-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="85832-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85832-127">-ResourceId</span></span>
<span data-ttu-id="85832-128">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="85832-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="85832-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85832-129">-Confirm</span></span>
<span data-ttu-id="85832-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85832-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85832-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85832-131">-WhatIf</span></span>
<span data-ttu-id="85832-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85832-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85832-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85832-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85832-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85832-134">CommonParameters</span></span>
<span data-ttu-id="85832-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85832-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85832-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85832-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85832-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85832-137">INPUTS</span></span>

### <span data-ttu-id="85832-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="85832-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="85832-139">System. String</span><span class="sxs-lookup"><span data-stu-id="85832-139">System.String</span></span>

## <span data-ttu-id="85832-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85832-140">OUTPUTS</span></span>

### <span data-ttu-id="85832-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85832-141">System.Boolean</span></span>

## <span data-ttu-id="85832-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85832-142">NOTES</span></span>

## <span data-ttu-id="85832-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85832-143">RELATED LINKS</span></span>
