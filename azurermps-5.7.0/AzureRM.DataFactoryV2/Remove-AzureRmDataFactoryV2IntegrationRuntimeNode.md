---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: bc16145569fd46b80e6d7a5afc1755f36346fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426729"
---
# <span data-ttu-id="c865a-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="c865a-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="c865a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c865a-102">SYNOPSIS</span></span>
<span data-ttu-id="c865a-103">Remover um nó com o nome fornecido em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c865a-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c865a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c865a-104">SYNTAX</span></span>

### <span data-ttu-id="c865a-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c865a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c865a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c865a-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c865a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c865a-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c865a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c865a-108">DESCRIPTION</span></span>
<span data-ttu-id="c865a-109">O cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode remove um nó em um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c865a-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="c865a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c865a-110">EXAMPLES</span></span>

### <span data-ttu-id="c865a-111">Exemplo 1: remover um nó de um tempo de execução de integração</span><span class="sxs-lookup"><span data-stu-id="c865a-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="c865a-112">Esse comando Remove um nó chamado ' Node_1 ' no tempo de execução de integração chamado ' test-selfhost-IV ' na assinatura do grupo de recursos chamado ' RG-Test-dfv2 ' e data Factory chamado ' test-DF-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="c865a-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="c865a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c865a-113">PARAMETERS</span></span>

### <span data-ttu-id="c865a-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c865a-114">-DataFactoryName</span></span>
<span data-ttu-id="c865a-115">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="c865a-115">The data factory name.</span></span>

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

### <span data-ttu-id="c865a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c865a-116">-DefaultProfile</span></span>
<span data-ttu-id="c865a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c865a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c865a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c865a-118">-Force</span></span>
<span data-ttu-id="c865a-119">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c865a-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c865a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c865a-120">-InputObject</span></span>
<span data-ttu-id="c865a-121">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c865a-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="c865a-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c865a-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c865a-123">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="c865a-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c865a-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c865a-124">-NodeName</span></span>
<span data-ttu-id="c865a-125">O nome do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c865a-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c865a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c865a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c865a-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c865a-127">The resource group name.</span></span>

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

### <span data-ttu-id="c865a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c865a-128">-ResourceId</span></span>
<span data-ttu-id="c865a-129">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="c865a-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c865a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c865a-130">-Confirm</span></span>
<span data-ttu-id="c865a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c865a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c865a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c865a-132">-WhatIf</span></span>
<span data-ttu-id="c865a-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c865a-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c865a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c865a-134">CommonParameters</span></span>
<span data-ttu-id="c865a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c865a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c865a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c865a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c865a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c865a-137">INPUTS</span></span>

### <span data-ttu-id="c865a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c865a-138">System.String</span></span>
<span data-ttu-id="c865a-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c865a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c865a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c865a-140">OUTPUTS</span></span>

### <span data-ttu-id="c865a-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="c865a-141">System.Object</span></span>

## <span data-ttu-id="c865a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c865a-142">NOTES</span></span>

## <span data-ttu-id="c865a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c865a-143">RELATED LINKS</span></span>

