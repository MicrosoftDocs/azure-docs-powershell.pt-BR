---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ae319662cf7b839524bd44524d63a3ba0a15fe20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429842"
---
# <span data-ttu-id="e4bca-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e4bca-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e4bca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4bca-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bca-103">Interrompe um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e4bca-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4bca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4bca-104">SYNTAX</span></span>

### <span data-ttu-id="e4bca-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4bca-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4bca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4bca-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bca-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e4bca-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4bca-108">DESCRIPTION</span></span>
<span data-ttu-id="e4bca-109">O cmdlet **Stop-AzureRmDataFactoryV2IntegrationRuntime** interrompe um tempo de execução de integração dedicada gerenciado no estado ' iniciado ', que foi iniciado pelo cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e4bca-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="e4bca-110">Os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="e4bca-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e4bca-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4bca-111">EXAMPLES</span></span>

### <span data-ttu-id="e4bca-112">Exemplo 1: parar um tempo de execução de integração gerenciada que está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="e4bca-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="e4bca-113">O tempo de execução de integração gerenciada ' test-reserlved-IV ' está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="e4bca-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="e4bca-114">Após a execução do cmdlet Stop-AzureRmDataFactoryV2IntegrationRuntime, os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="e4bca-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e4bca-115">OS</span><span class="sxs-lookup"><span data-stu-id="e4bca-115">PARAMETERS</span></span>

### <span data-ttu-id="e4bca-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e4bca-116">-DataFactoryName</span></span>
<span data-ttu-id="e4bca-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e4bca-117">The data factory name.</span></span>

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

### <span data-ttu-id="e4bca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bca-118">-DefaultProfile</span></span>
<span data-ttu-id="e4bca-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4bca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e4bca-120">-Force</span></span>
<span data-ttu-id="e4bca-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e4bca-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e4bca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4bca-122">-InputObject</span></span>
<span data-ttu-id="e4bca-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="e4bca-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="e4bca-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4bca-124">-Name</span></span>
<span data-ttu-id="e4bca-125">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="e4bca-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="e4bca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4bca-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4bca-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4bca-127">The resource group name.</span></span>

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

### <span data-ttu-id="e4bca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4bca-128">-ResourceId</span></span>
<span data-ttu-id="e4bca-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bca-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e4bca-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4bca-130">-Confirm</span></span>
<span data-ttu-id="e4bca-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bca-132">-WhatIf</span></span>
<span data-ttu-id="e4bca-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bca-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e4bca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bca-134">CommonParameters</span></span>
<span data-ttu-id="e4bca-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bca-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bca-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bca-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4bca-137">INPUTS</span></span>

### <span data-ttu-id="e4bca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e4bca-138">System.String</span></span>
<span data-ttu-id="e4bca-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e4bca-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e4bca-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4bca-140">OUTPUTS</span></span>

### <span data-ttu-id="e4bca-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4bca-141">System.Boolean</span></span>

## <span data-ttu-id="e4bca-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4bca-142">NOTES</span></span>
<span data-ttu-id="e4bca-143">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="e4bca-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e4bca-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4bca-144">RELATED LINKS</span></span>

[<span data-ttu-id="e4bca-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e4bca-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
