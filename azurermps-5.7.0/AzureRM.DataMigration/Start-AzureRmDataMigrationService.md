---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426708"
---
# <span data-ttu-id="757a6-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="757a6-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="757a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="757a6-102">SYNOPSIS</span></span>
<span data-ttu-id="757a6-103">Inicia uma instância do serviço de migração do banco de dados do Azure em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="757a6-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="757a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="757a6-104">SYNTAX</span></span>

### <span data-ttu-id="757a6-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="757a6-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="757a6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="757a6-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="757a6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="757a6-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="757a6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="757a6-108">DESCRIPTION</span></span>
<span data-ttu-id="757a6-109">O cmdlet Start-AzureRmDataMigrationService inicia uma instância do serviço de migração do banco de dados do Azure em um estado interrompido.</span><span class="sxs-lookup"><span data-stu-id="757a6-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="757a6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="757a6-110">EXAMPLES</span></span>

### <span data-ttu-id="757a6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="757a6-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="757a6-112">O exemplo acima inicia uma instância do serviço de migração de banco de dados do Azure chamada serviço de teste em um estado parado com base no nome do serviço passado como entrada</span><span class="sxs-lookup"><span data-stu-id="757a6-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="757a6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="757a6-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="757a6-114">O exemplo acima inicia uma instância do serviço de migração do banco de dados do Azure com base no PSDataMigrationService passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="757a6-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="757a6-115">OS</span><span class="sxs-lookup"><span data-stu-id="757a6-115">PARAMETERS</span></span>

### <span data-ttu-id="757a6-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="757a6-116">-Confirm</span></span>
<span data-ttu-id="757a6-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="757a6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757a6-118">-DefaultProfile</span></span>
<span data-ttu-id="757a6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="757a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="757a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="757a6-120">-InputObject</span></span>
<span data-ttu-id="757a6-121">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="757a6-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="757a6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="757a6-122">-Name</span></span>
<span data-ttu-id="757a6-123">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="757a6-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="757a6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="757a6-124">-PassThru</span></span>
<span data-ttu-id="757a6-125">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="757a6-125">Returns an true/false.</span></span>
<span data-ttu-id="757a6-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="757a6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="757a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="757a6-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="757a6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="757a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="757a6-129">-ResourceId</span></span>
<span data-ttu-id="757a6-130">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="757a6-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="757a6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757a6-131">-WhatIf</span></span>
<span data-ttu-id="757a6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="757a6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757a6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="757a6-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="757a6-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="757a6-134">INPUTS</span></span>

### <span data-ttu-id="757a6-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="757a6-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="757a6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="757a6-136">System.String</span></span>


## <span data-ttu-id="757a6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="757a6-137">OUTPUTS</span></span>

### <span data-ttu-id="757a6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="757a6-138">System.Boolean</span></span>


## <span data-ttu-id="757a6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="757a6-139">NOTES</span></span>

## <span data-ttu-id="757a6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="757a6-140">RELATED LINKS</span></span>


