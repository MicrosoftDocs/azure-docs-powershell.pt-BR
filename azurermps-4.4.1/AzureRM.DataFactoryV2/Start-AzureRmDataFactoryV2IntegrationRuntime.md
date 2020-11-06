---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611127"
---
# <span data-ttu-id="8f7d8-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f7d8-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="8f7d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7d8-103">Inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f7d8-104">SYNTAX</span></span>

### <span data-ttu-id="8f7d8-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f7d8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8f7d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7d8-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8f7d8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8f7d8-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="8f7d8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f7d8-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7d8-109">O cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="8f7d8-110">O recurso é provisionado e após a operação em que o estado é ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="8f7d8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f7d8-111">EXAMPLES</span></span>

### <span data-ttu-id="8f7d8-112">Exemplo 1: iniciar um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="8f7d8-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="8f7d8-113">Este cmdlet inicia um tempo de execução de integração dedicada gerenciado chamado ' test-Dedicated-IV '.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="8f7d8-114">OS</span><span class="sxs-lookup"><span data-stu-id="8f7d8-114">PARAMETERS</span></span>

### <span data-ttu-id="8f7d8-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f7d8-115">-Confirm</span></span>
<span data-ttu-id="8f7d8-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7d8-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8f7d8-117">-DataFactoryName</span></span>
<span data-ttu-id="8f7d8-118">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-118">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7d8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8f7d8-119">-Force</span></span>
<span data-ttu-id="8f7d8-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8f7d8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f7d8-121">-InputObject</span></span>
<span data-ttu-id="8f7d8-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7d8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f7d8-123">-Name</span></span>
<span data-ttu-id="8f7d8-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f7d8-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7d8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f7d8-127">-ResourceId</span></span>
<span data-ttu-id="8f7d8-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7d8-129">-WhatIf</span></span>
<span data-ttu-id="8f7d8-130">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7d8-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="8f7d8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f7d8-131">INPUTS</span></span>

### <span data-ttu-id="8f7d8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f7d8-132">System.String</span></span>
<span data-ttu-id="8f7d8-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f7d8-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8f7d8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f7d8-134">OUTPUTS</span></span>

### <span data-ttu-id="8f7d8-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="8f7d8-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="8f7d8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f7d8-136">NOTES</span></span>

## <span data-ttu-id="8f7d8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7d8-137">RELATED LINKS</span></span>
[<span data-ttu-id="8f7d8-138">Parar-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f7d8-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
