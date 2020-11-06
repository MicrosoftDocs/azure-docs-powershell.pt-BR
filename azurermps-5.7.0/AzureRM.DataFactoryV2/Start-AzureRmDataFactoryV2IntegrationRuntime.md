---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 77c06c871d35223f296a7f318460b868e8ad0320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427571"
---
# <span data-ttu-id="e2fa2-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2fa2-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e2fa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fa2-103">Inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2fa2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2fa2-104">SYNTAX</span></span>

### <span data-ttu-id="e2fa2-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2fa2-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2fa2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2fa2-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2fa2-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e2fa2-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2fa2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2fa2-108">DESCRIPTION</span></span>
<span data-ttu-id="e2fa2-109">O cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="e2fa2-110">O recurso é provisionado e após a operação em que o estado é ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="e2fa2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2fa2-111">EXAMPLES</span></span>

### <span data-ttu-id="e2fa2-112">Exemplo 1: iniciar um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="e2fa2-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="e2fa2-113">Este cmdlet inicia um tempo de execução de integração dedicada gerenciado chamado ' test-Dedicated-IV '.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="e2fa2-114">OS</span><span class="sxs-lookup"><span data-stu-id="e2fa2-114">PARAMETERS</span></span>

### <span data-ttu-id="e2fa2-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e2fa2-115">-DataFactoryName</span></span>
<span data-ttu-id="e2fa2-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-116">The data factory name.</span></span>

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

### <span data-ttu-id="e2fa2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fa2-117">-DefaultProfile</span></span>
<span data-ttu-id="e2fa2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2fa2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e2fa2-119">-Force</span></span>
<span data-ttu-id="e2fa2-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e2fa2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2fa2-121">-InputObject</span></span>
<span data-ttu-id="e2fa2-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e2fa2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2fa2-123">-Name</span></span>
<span data-ttu-id="e2fa2-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="e2fa2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2fa2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2fa2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-126">The resource group name.</span></span>

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

### <span data-ttu-id="e2fa2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2fa2-127">-ResourceId</span></span>
<span data-ttu-id="e2fa2-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e2fa2-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2fa2-129">-Confirm</span></span>
<span data-ttu-id="e2fa2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2fa2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2fa2-131">-WhatIf</span></span>
<span data-ttu-id="e2fa2-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e2fa2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fa2-133">CommonParameters</span></span>
<span data-ttu-id="e2fa2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fa2-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2fa2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fa2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2fa2-136">INPUTS</span></span>

### <span data-ttu-id="e2fa2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e2fa2-137">System.String</span></span>
<span data-ttu-id="e2fa2-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2fa2-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e2fa2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2fa2-139">OUTPUTS</span></span>

### <span data-ttu-id="e2fa2-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e2fa2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e2fa2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2fa2-141">NOTES</span></span>

## <span data-ttu-id="e2fa2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2fa2-142">RELATED LINKS</span></span>

[<span data-ttu-id="e2fa2-143">Parar-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e2fa2-143">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()