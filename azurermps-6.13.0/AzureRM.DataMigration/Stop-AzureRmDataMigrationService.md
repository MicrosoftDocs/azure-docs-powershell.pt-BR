---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429568"
---
# <span data-ttu-id="ff01a-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff01a-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="ff01a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff01a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff01a-103">Interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="ff01a-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff01a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff01a-104">SYNTAX</span></span>

### <span data-ttu-id="ff01a-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff01a-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff01a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff01a-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff01a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff01a-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff01a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff01a-108">DESCRIPTION</span></span>
<span data-ttu-id="ff01a-109">O cmdlet Stop-AzureRmDataMigrationService interrompe uma instância do serviço de migração de banco de dados do Azure que está em um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="ff01a-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="ff01a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff01a-110">EXAMPLES</span></span>

### <span data-ttu-id="ff01a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff01a-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ff01a-112">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure chamado TestService com base no nome do serviço passado como parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="ff01a-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="ff01a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ff01a-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="ff01a-114">O exemplo acima interrompe uma instância do serviço de migração de banco de dados do Azure com base no objeto PSDataMigrationService passado como parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="ff01a-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="ff01a-115">OS</span><span class="sxs-lookup"><span data-stu-id="ff01a-115">PARAMETERS</span></span>

### <span data-ttu-id="ff01a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff01a-116">-DefaultProfile</span></span>
<span data-ttu-id="ff01a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff01a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff01a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff01a-118">-InputObject</span></span>
<span data-ttu-id="ff01a-119">Objeto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="ff01a-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ff01a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff01a-120">-Name</span></span>
<span data-ttu-id="ff01a-121">Nome do serviço de migração de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ff01a-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ff01a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff01a-122">-PassThru</span></span>
<span data-ttu-id="ff01a-123">Retorna verdadeiro/falso.</span><span class="sxs-lookup"><span data-stu-id="ff01a-123">Returns an true/false.</span></span>
<span data-ttu-id="ff01a-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ff01a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ff01a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff01a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff01a-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff01a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff01a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff01a-127">-ResourceId</span></span>
<span data-ttu-id="ff01a-128">DataMigrationService ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ff01a-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ff01a-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff01a-129">-Confirm</span></span>
<span data-ttu-id="ff01a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff01a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff01a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff01a-131">-WhatIf</span></span>
<span data-ttu-id="ff01a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff01a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff01a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff01a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff01a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff01a-134">CommonParameters</span></span>
<span data-ttu-id="ff01a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff01a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff01a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff01a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff01a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff01a-137">INPUTS</span></span>

### <span data-ttu-id="ff01a-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ff01a-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="ff01a-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff01a-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ff01a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff01a-140">System.String</span></span>

## <span data-ttu-id="ff01a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff01a-141">OUTPUTS</span></span>

### <span data-ttu-id="ff01a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff01a-142">System.Boolean</span></span>

## <span data-ttu-id="ff01a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff01a-143">NOTES</span></span>

## <span data-ttu-id="ff01a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff01a-144">RELATED LINKS</span></span>
