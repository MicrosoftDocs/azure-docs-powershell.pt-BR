---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 24c5f3b93b2be446eed4e5b81e1e69bf2116aa8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886632"
---
# <span data-ttu-id="35767-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35767-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="35767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35767-102">SYNOPSIS</span></span>
<span data-ttu-id="35767-103">Remove uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="35767-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35767-104">SYNTAX</span></span>

### <span data-ttu-id="35767-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="35767-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35767-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35767-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35767-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35767-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35767-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35767-108">DESCRIPTION</span></span>
<span data-ttu-id="35767-109">O cmdlet **Remove-AzIntegrationAccountBatchConfiguration** remove uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="35767-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35767-110">EXAMPLES</span></span>

### <span data-ttu-id="35767-111">Exemplo 1: Remover uma configuração em lote por parâmetros</span><span class="sxs-lookup"><span data-stu-id="35767-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="35767-112">Remove a configuração em lote denominada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="35767-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="35767-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35767-113">PARAMETERS</span></span>

### <span data-ttu-id="35767-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35767-114">-DefaultProfile</span></span>
<span data-ttu-id="35767-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35767-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35767-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35767-116">-InputObject</span></span>
<span data-ttu-id="35767-117">Uma configuração em lotes de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35767-118">-Name</span><span class="sxs-lookup"><span data-stu-id="35767-118">-Name</span></span>
<span data-ttu-id="35767-119">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35767-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="35767-120">-ParentName</span></span>
<span data-ttu-id="35767-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35767-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35767-122">-PassThru</span></span>
<span data-ttu-id="35767-123">Retorne se o comando foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="35767-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="35767-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35767-124">-ResourceGroupName</span></span>
<span data-ttu-id="35767-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35767-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35767-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35767-126">-ResourceId</span></span>
<span data-ttu-id="35767-127">A ID do recurso de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35767-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35767-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35767-128">-Confirm</span></span>
<span data-ttu-id="35767-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35767-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35767-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35767-130">-WhatIf</span></span>
<span data-ttu-id="35767-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35767-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35767-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35767-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35767-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35767-133">CommonParameters</span></span>
<span data-ttu-id="35767-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35767-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35767-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35767-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35767-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35767-136">INPUTS</span></span>

### <span data-ttu-id="35767-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35767-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="35767-138">System.String</span><span class="sxs-lookup"><span data-stu-id="35767-138">System.String</span></span>

## <span data-ttu-id="35767-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35767-139">OUTPUTS</span></span>

### <span data-ttu-id="35767-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35767-140">System.Boolean</span></span>

## <span data-ttu-id="35767-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="35767-141">NOTES</span></span>

## <span data-ttu-id="35767-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35767-142">RELATED LINKS</span></span>
