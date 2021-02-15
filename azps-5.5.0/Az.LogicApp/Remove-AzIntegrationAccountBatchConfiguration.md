---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113015"
---
# <span data-ttu-id="fd908-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd908-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fd908-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd908-102">SYNOPSIS</span></span>
<span data-ttu-id="fd908-103">Remove uma configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="fd908-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd908-104">SYNTAX</span></span>

### <span data-ttu-id="fd908-105">ByIntegrationAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd908-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd908-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd908-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd908-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd908-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd908-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd908-108">DESCRIPTION</span></span>
<span data-ttu-id="fd908-109">O cmdlet **Remove-AzIntegrationAccountBatchConfiguration** remove uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="fd908-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd908-110">EXAMPLES</span></span>

### <span data-ttu-id="fd908-111">Exemplo 1: Remover uma configuração em lotes por parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd908-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="fd908-112">Remove a configuração em lotes chamada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="fd908-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="fd908-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd908-113">PARAMETERS</span></span>

### <span data-ttu-id="fd908-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd908-114">-DefaultProfile</span></span>
<span data-ttu-id="fd908-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd908-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd908-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd908-116">-InputObject</span></span>
<span data-ttu-id="fd908-117">Uma configuração em lotes de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="fd908-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd908-118">-Name</span></span>
<span data-ttu-id="fd908-119">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="fd908-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="fd908-120">-ParentName</span></span>
<span data-ttu-id="fd908-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-121">The integration account name.</span></span>

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

### <span data-ttu-id="fd908-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd908-122">-PassThru</span></span>
<span data-ttu-id="fd908-123">Retorne se o comando foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="fd908-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="fd908-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd908-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd908-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd908-125">The resource group name.</span></span>

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

### <span data-ttu-id="fd908-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd908-126">-ResourceId</span></span>
<span data-ttu-id="fd908-127">A ID do recurso de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="fd908-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="fd908-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd908-128">-Confirm</span></span>
<span data-ttu-id="fd908-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd908-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd908-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd908-130">-WhatIf</span></span>
<span data-ttu-id="fd908-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd908-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd908-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd908-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd908-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd908-133">CommonParameters</span></span>
<span data-ttu-id="fd908-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd908-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd908-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd908-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd908-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd908-136">INPUTS</span></span>

### <span data-ttu-id="fd908-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd908-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="fd908-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fd908-138">System.String</span></span>

## <span data-ttu-id="fd908-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd908-139">OUTPUTS</span></span>

### <span data-ttu-id="fd908-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd908-140">System.Boolean</span></span>

## <span data-ttu-id="fd908-141">Notas</span><span class="sxs-lookup"><span data-stu-id="fd908-141">NOTES</span></span>

## <span data-ttu-id="fd908-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd908-142">RELATED LINKS</span></span>
