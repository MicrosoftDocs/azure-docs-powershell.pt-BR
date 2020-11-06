---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a9254fbac7e0c98413f4367d9b5e62581f6cb64c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602618"
---
# <span data-ttu-id="a87ee-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a87ee-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="a87ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a87ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a87ee-103">Inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a87ee-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a87ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a87ee-104">SYNTAX</span></span>

### <span data-ttu-id="a87ee-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a87ee-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a87ee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a87ee-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a87ee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a87ee-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a87ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a87ee-108">DESCRIPTION</span></span>
<span data-ttu-id="a87ee-109">O cmdlet **Start-AzureRmDataFactoryV2IntegrationRuntime** inicia um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a87ee-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="a87ee-110">O recurso é provisionado e após a operação em que o estado é ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="a87ee-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="a87ee-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a87ee-111">EXAMPLES</span></span>

### <span data-ttu-id="a87ee-112">Exemplo 1: iniciar um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="a87ee-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="a87ee-113">Este cmdlet inicia um tempo de execução de integração dedicada gerenciado chamado ' test-Dedicated-IV '.</span><span class="sxs-lookup"><span data-stu-id="a87ee-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="a87ee-114">OS</span><span class="sxs-lookup"><span data-stu-id="a87ee-114">PARAMETERS</span></span>

### <span data-ttu-id="a87ee-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a87ee-115">-DataFactoryName</span></span>
<span data-ttu-id="a87ee-116">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="a87ee-116">The data factory name.</span></span>

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

### <span data-ttu-id="a87ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87ee-117">-DefaultProfile</span></span>
<span data-ttu-id="a87ee-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a87ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a87ee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a87ee-119">-Force</span></span>
<span data-ttu-id="a87ee-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a87ee-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a87ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a87ee-121">-InputObject</span></span>
<span data-ttu-id="a87ee-122">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="a87ee-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="a87ee-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a87ee-123">-Name</span></span>
<span data-ttu-id="a87ee-124">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="a87ee-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="a87ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a87ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="a87ee-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a87ee-126">The resource group name.</span></span>

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

### <span data-ttu-id="a87ee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a87ee-127">-ResourceId</span></span>
<span data-ttu-id="a87ee-128">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="a87ee-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a87ee-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a87ee-129">-Confirm</span></span>
<span data-ttu-id="a87ee-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a87ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87ee-131">-WhatIf</span></span>
<span data-ttu-id="a87ee-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87ee-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a87ee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87ee-133">CommonParameters</span></span>
<span data-ttu-id="a87ee-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87ee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87ee-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87ee-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87ee-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a87ee-136">INPUTS</span></span>

### <span data-ttu-id="a87ee-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a87ee-137">System.String</span></span>

### <span data-ttu-id="a87ee-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a87ee-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="a87ee-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a87ee-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a87ee-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a87ee-140">OUTPUTS</span></span>

### <span data-ttu-id="a87ee-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="a87ee-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="a87ee-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a87ee-142">NOTES</span></span>

## <span data-ttu-id="a87ee-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a87ee-143">RELATED LINKS</span></span>

[<span data-ttu-id="a87ee-144">Parar-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a87ee-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
