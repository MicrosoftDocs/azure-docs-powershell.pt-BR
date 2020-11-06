---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441345"
---
# <span data-ttu-id="1cfce-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1cfce-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="1cfce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cfce-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfce-103">Interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="1cfce-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cfce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cfce-104">SYNTAX</span></span>

### <span data-ttu-id="1cfce-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1cfce-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1cfce-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfce-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1cfce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfce-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1cfce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cfce-108">DESCRIPTION</span></span>
<span data-ttu-id="1cfce-109">O cmdlet Stop-AzureRmDataMigrationService interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="1cfce-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="1cfce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cfce-110">EXAMPLES</span></span>

### <span data-ttu-id="1cfce-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1cfce-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="1cfce-112">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure chamado TestService com base no nome do serviço passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="1cfce-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="1cfce-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1cfce-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="1cfce-114">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure com base no objeto PSDataMigrationService passado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="1cfce-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="1cfce-115">OS</span><span class="sxs-lookup"><span data-stu-id="1cfce-115">PARAMETERS</span></span>

### <span data-ttu-id="1cfce-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1cfce-116">-Confirm</span></span>
<span data-ttu-id="1cfce-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cfce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfce-118">-DefaultProfile</span></span>
<span data-ttu-id="1cfce-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cfce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cfce-120">-InputObject</span></span>
<span data-ttu-id="1cfce-121">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="1cfce-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="1cfce-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cfce-122">-Name</span></span>
<span data-ttu-id="1cfce-123">Nome do serviço de migração de dados.</span><span class="sxs-lookup"><span data-stu-id="1cfce-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="1cfce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cfce-124">-PassThru</span></span>
<span data-ttu-id="1cfce-125">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="1cfce-125">Returns an true/false.</span></span>
<span data-ttu-id="1cfce-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1cfce-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1cfce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfce-127">-ResourceGroupName</span></span>
<span data-ttu-id="1cfce-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cfce-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1cfce-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cfce-129">-ResourceId</span></span>
<span data-ttu-id="1cfce-130">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1cfce-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="1cfce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cfce-131">-WhatIf</span></span>
<span data-ttu-id="1cfce-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cfce-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cfce-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cfce-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1cfce-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cfce-134">INPUTS</span></span>

### <span data-ttu-id="1cfce-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1cfce-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="1cfce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfce-136">System.String</span></span>


## <span data-ttu-id="1cfce-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cfce-137">OUTPUTS</span></span>

### <span data-ttu-id="1cfce-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cfce-138">System.Boolean</span></span>


## <span data-ttu-id="1cfce-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cfce-139">NOTES</span></span>

## <span data-ttu-id="1cfce-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cfce-140">RELATED LINKS</span></span>

