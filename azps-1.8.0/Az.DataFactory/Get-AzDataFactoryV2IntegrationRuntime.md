---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601157"
---
# <span data-ttu-id="07213-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="07213-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07213-102">SYNOPSIS</span></span>
<span data-ttu-id="07213-103">Obtém informações sobre os recursos do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="07213-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="07213-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07213-104">SYNTAX</span></span>

### <span data-ttu-id="07213-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="07213-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07213-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07213-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07213-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="07213-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07213-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07213-108">DESCRIPTION</span></span>
<span data-ttu-id="07213-109">O cmdlet Get-AzDataFactoryV2IntegrationRuntime Obtém informações sobre os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="07213-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="07213-110">Se você especificar o nome de um tempo de execução de integração, esse cmdlet obterá informações sobre esse tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="07213-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="07213-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os tempos de execução de integração em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="07213-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="07213-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07213-112">EXAMPLES</span></span>

### <span data-ttu-id="07213-113">Exemplo 1: listar todos os tempos de execução de integração em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="07213-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="07213-114">Liste todos os tempos de execução de integração na fábrica de dados chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="07213-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="07213-115">Exemplo 2: obter tempo de execução de integração dedicada gerenciado</span><span class="sxs-lookup"><span data-stu-id="07213-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="07213-116">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="07213-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="07213-117">Exemplo 3: obter tempo de execução de integração dedicada gerenciado com status detalhado</span><span class="sxs-lookup"><span data-stu-id="07213-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="07213-118">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="07213-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="07213-119">Exemplo 4: obter o tempo de execução de integração de hospedagem interna</span><span class="sxs-lookup"><span data-stu-id="07213-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="07213-120">Este comando exibe informações sobre o tempo de execução de integração chamado ' test-Dedicated-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="07213-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="07213-121">OS</span><span class="sxs-lookup"><span data-stu-id="07213-121">PARAMETERS</span></span>

### <span data-ttu-id="07213-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="07213-122">-DataFactoryName</span></span>
<span data-ttu-id="07213-123">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="07213-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07213-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07213-124">-DefaultProfile</span></span>
<span data-ttu-id="07213-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07213-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07213-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07213-126">-InputObject</span></span>
<span data-ttu-id="07213-127">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="07213-127">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07213-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="07213-128">-Name</span></span>
<span data-ttu-id="07213-129">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="07213-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07213-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07213-130">-ResourceGroupName</span></span>
<span data-ttu-id="07213-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07213-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07213-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07213-132">-ResourceId</span></span>
<span data-ttu-id="07213-133">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="07213-133">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07213-134">-Status</span><span class="sxs-lookup"><span data-stu-id="07213-134">-Status</span></span>
<span data-ttu-id="07213-135">O status do detalhe do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="07213-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="07213-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07213-136">CommonParameters</span></span>
<span data-ttu-id="07213-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07213-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07213-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07213-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07213-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07213-139">INPUTS</span></span>

### <span data-ttu-id="07213-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07213-140">System.String</span></span>

### <span data-ttu-id="07213-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="07213-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07213-142">OUTPUTS</span></span>

### <span data-ttu-id="07213-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="07213-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="07213-145">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="07213-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="07213-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07213-147">NOTES</span></span>
<span data-ttu-id="07213-148">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="07213-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="07213-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07213-149">RELATED LINKS</span></span>

[<span data-ttu-id="07213-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="07213-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="07213-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
