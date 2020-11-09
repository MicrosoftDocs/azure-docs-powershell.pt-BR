---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280946"
---
# <span data-ttu-id="6eaa9-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6eaa9-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6eaa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eaa9-103">Interrompe um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="6eaa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eaa9-104">SYNTAX</span></span>

### <span data-ttu-id="6eaa9-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6eaa9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eaa9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6eaa9-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eaa9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6eaa9-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eaa9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6eaa9-108">DESCRIPTION</span></span>
<span data-ttu-id="6eaa9-109">O cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** interrompe um tempo de execução de integração dedicada gerenciado no estado ' iniciado ', que foi iniciado pelo cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="6eaa9-110">Os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="6eaa9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6eaa9-111">EXAMPLES</span></span>

### <span data-ttu-id="6eaa9-112">Exemplo 1: parar um tempo de execução de integração gerenciada que está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="6eaa9-113">O tempo de execução de integração gerenciada ' test-reserlved-IV ' está no estado ' iniciado '.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="6eaa9-114">Após a execução do cmdlet Stop-AzDataFactoryV2IntegrationRuntime, os recursos são liberados e o estado é transferido para ' parado '.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="6eaa9-115">OS</span><span class="sxs-lookup"><span data-stu-id="6eaa9-115">PARAMETERS</span></span>

### <span data-ttu-id="6eaa9-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6eaa9-116">-DataFactoryName</span></span>
<span data-ttu-id="6eaa9-117">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-117">The data factory name.</span></span>

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

### <span data-ttu-id="6eaa9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eaa9-118">-DefaultProfile</span></span>
<span data-ttu-id="6eaa9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eaa9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6eaa9-120">-Force</span></span>
<span data-ttu-id="6eaa9-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6eaa9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eaa9-122">-InputObject</span></span>
<span data-ttu-id="6eaa9-123">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="6eaa9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eaa9-124">-Name</span></span>
<span data-ttu-id="6eaa9-125">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="6eaa9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eaa9-126">-ResourceGroupName</span></span>
<span data-ttu-id="6eaa9-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-127">The resource group name.</span></span>

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

### <span data-ttu-id="6eaa9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eaa9-128">-ResourceId</span></span>
<span data-ttu-id="6eaa9-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6eaa9-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6eaa9-130">-Confirm</span></span>
<span data-ttu-id="6eaa9-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eaa9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eaa9-132">-WhatIf</span></span>
<span data-ttu-id="6eaa9-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6eaa9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eaa9-134">CommonParameters</span></span>
<span data-ttu-id="6eaa9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eaa9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eaa9-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eaa9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eaa9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6eaa9-137">INPUTS</span></span>

### <span data-ttu-id="6eaa9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6eaa9-138">System.String</span></span>

### <span data-ttu-id="6eaa9-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6eaa9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6eaa9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6eaa9-140">OUTPUTS</span></span>

### <span data-ttu-id="6eaa9-141">System. void</span><span class="sxs-lookup"><span data-stu-id="6eaa9-141">System.Void</span></span>

## <span data-ttu-id="6eaa9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6eaa9-142">NOTES</span></span>
<span data-ttu-id="6eaa9-143">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, data, fábricas, Copy, Activities, tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="6eaa9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="6eaa9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eaa9-144">RELATED LINKS</span></span>

[<span data-ttu-id="6eaa9-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6eaa9-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
