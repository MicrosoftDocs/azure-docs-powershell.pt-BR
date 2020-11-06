---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce9ca0f1581bc995f9ea18b3b87169ed979dd92c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440065"
---
# <span data-ttu-id="7e855-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e855-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="7e855-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e855-102">SYNOPSIS</span></span>
<span data-ttu-id="7e855-103">Interrompe um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7e855-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e855-104">SYNTAX</span></span>

### <span data-ttu-id="7e855-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e855-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e855-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e855-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e855-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7e855-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e855-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e855-108">DESCRIPTION</span></span>
<span data-ttu-id="7e855-109">O cmdlet **Stop-AzureRmDataFactoryV2IntegrationRuntime** interrompe um tempo de execução de integração dedicada gerenciado no estado ' iniciado ', que foi iniciado pelo cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="7e855-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="7e855-110">Os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="7e855-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="7e855-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e855-111">EXAMPLES</span></span>

### <span data-ttu-id="7e855-112">Exemplo 1: parar um tempo de execução de integração gerenciada que está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="7e855-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="7e855-113">O tempo de execução de integração gerenciada ' test-reserlved-IV ' está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="7e855-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="7e855-114">Após a execução do cmdlet Stop-AzureRmDataFactoryV2IntegrationRuntime, os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="7e855-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="7e855-115">OS</span><span class="sxs-lookup"><span data-stu-id="7e855-115">PARAMETERS</span></span>

### <span data-ttu-id="7e855-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7e855-116">-DataFactoryName</span></span>
<span data-ttu-id="7e855-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="7e855-117">The data factory name.</span></span>

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

### <span data-ttu-id="7e855-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e855-118">-DefaultProfile</span></span>
<span data-ttu-id="7e855-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e855-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e855-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e855-120">-Force</span></span>
<span data-ttu-id="7e855-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="7e855-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7e855-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e855-122">-InputObject</span></span>
<span data-ttu-id="7e855-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="7e855-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="7e855-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e855-124">-Name</span></span>
<span data-ttu-id="7e855-125">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="7e855-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="7e855-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e855-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e855-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e855-127">The resource group name.</span></span>

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

### <span data-ttu-id="7e855-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e855-128">-ResourceId</span></span>
<span data-ttu-id="7e855-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e855-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7e855-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e855-130">-Confirm</span></span>
<span data-ttu-id="7e855-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e855-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e855-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e855-132">-WhatIf</span></span>
<span data-ttu-id="7e855-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e855-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7e855-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e855-134">CommonParameters</span></span>
<span data-ttu-id="7e855-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e855-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e855-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e855-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e855-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e855-137">INPUTS</span></span>

### <span data-ttu-id="7e855-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7e855-138">System.String</span></span>

### <span data-ttu-id="7e855-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e855-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="7e855-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e855-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7e855-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e855-141">OUTPUTS</span></span>

### <span data-ttu-id="7e855-142">System. void</span><span class="sxs-lookup"><span data-stu-id="7e855-142">System.Void</span></span>

## <span data-ttu-id="7e855-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e855-143">NOTES</span></span>
<span data-ttu-id="7e855-144">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="7e855-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="7e855-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e855-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e855-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e855-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
