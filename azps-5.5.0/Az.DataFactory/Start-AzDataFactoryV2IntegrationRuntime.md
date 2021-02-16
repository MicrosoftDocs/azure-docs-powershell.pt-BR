---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113275"
---
# <span data-ttu-id="ec8b5-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ec8b5-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ec8b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8b5-103">Inicia um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="ec8b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec8b5-104">SYNTAX</span></span>

### <span data-ttu-id="ec8b5-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec8b5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec8b5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8b5-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec8b5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ec8b5-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec8b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec8b5-108">DESCRIPTION</span></span>
<span data-ttu-id="ec8b5-109">O cmdlet **Start-AzDataFactoryV2IntegrationRuntime** inicia um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="ec8b5-110">O recurso é provisionado e, após a operação, o estado é "Iniciado".</span><span class="sxs-lookup"><span data-stu-id="ec8b5-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="ec8b5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec8b5-111">EXAMPLES</span></span>

### <span data-ttu-id="ec8b5-112">Exemplo 1: Iniciar um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="ec8b5-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

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
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="ec8b5-113">Este cmdlet inicia um tempo de execução de integração dedicado gerenciado chamado "test-dedicated-ir".</span><span class="sxs-lookup"><span data-stu-id="ec8b5-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="ec8b5-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec8b5-114">PARAMETERS</span></span>

### <span data-ttu-id="ec8b5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ec8b5-115">-DataFactoryName</span></span>
<span data-ttu-id="ec8b5-116">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-116">The data factory name.</span></span>

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

### <span data-ttu-id="ec8b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8b5-117">-DefaultProfile</span></span>
<span data-ttu-id="ec8b5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec8b5-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="ec8b5-119">-Force</span></span>
<span data-ttu-id="ec8b5-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ec8b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec8b5-121">-InputObject</span></span>
<span data-ttu-id="ec8b5-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="ec8b5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec8b5-123">-Name</span></span>
<span data-ttu-id="ec8b5-124">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec8b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ec8b5-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-126">The resource group name.</span></span>

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

### <span data-ttu-id="ec8b5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec8b5-127">-ResourceId</span></span>
<span data-ttu-id="ec8b5-128">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ec8b5-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ec8b5-129">-Confirm</span></span>
<span data-ttu-id="ec8b5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec8b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec8b5-131">-WhatIf</span></span>
<span data-ttu-id="ec8b5-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ec8b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8b5-133">CommonParameters</span></span>
<span data-ttu-id="ec8b5-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8b5-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8b5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8b5-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="ec8b5-136">INPUTS</span></span>

### <span data-ttu-id="ec8b5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ec8b5-137">System.String</span></span>

### <span data-ttu-id="ec8b5-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ec8b5-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ec8b5-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ec8b5-139">OUTPUTS</span></span>

### <span data-ttu-id="ec8b5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="ec8b5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ec8b5-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ec8b5-141">NOTES</span></span>

## <span data-ttu-id="ec8b5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec8b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="ec8b5-143">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ec8b5-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
