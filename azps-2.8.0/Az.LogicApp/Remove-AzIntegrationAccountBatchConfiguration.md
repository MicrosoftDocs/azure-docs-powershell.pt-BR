---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: e2c4f3f399bd4bcd472ae04c6ca2234c2d2b26d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596033"
---
# <span data-ttu-id="5f3f9-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3f9-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="5f3f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3f9-103">Remove uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="5f3f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f3f9-104">SYNTAX</span></span>

### <span data-ttu-id="5f3f9-105">ByIntegrationAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="5f3f9-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3f9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f3f9-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3f9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f3f9-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f3f9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f3f9-108">DESCRIPTION</span></span>
<span data-ttu-id="5f3f9-109">O cmdlet **Remove-AzIntegrationAccountBatchConfiguration** remove uma configuração em lotes de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="5f3f9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f3f9-110">EXAMPLES</span></span>

### <span data-ttu-id="5f3f9-111">Exemplo 1: remover uma configuração em lotes por parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f3f9-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="5f3f9-112">Remove a configuração em lotes chamada "sampleBatchConfig" localizada na conta de integração "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="5f3f9-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="5f3f9-113">OS</span><span class="sxs-lookup"><span data-stu-id="5f3f9-113">PARAMETERS</span></span>

### <span data-ttu-id="5f3f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3f9-114">-DefaultProfile</span></span>
<span data-ttu-id="5f3f9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f3f9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f3f9-116">-InputObject</span></span>
<span data-ttu-id="5f3f9-117">Uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="5f3f9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f3f9-118">-Name</span></span>
<span data-ttu-id="5f3f9-119">O nome de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="5f3f9-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="5f3f9-120">-ParentName</span></span>
<span data-ttu-id="5f3f9-121">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-121">The integration account name.</span></span>

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

### <span data-ttu-id="5f3f9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f3f9-122">-PassThru</span></span>
<span data-ttu-id="5f3f9-123">Retorna se o comando foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="5f3f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f3f9-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-125">The resource group name.</span></span>

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

### <span data-ttu-id="5f3f9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f3f9-126">-ResourceId</span></span>
<span data-ttu-id="5f3f9-127">A ID do recurso de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="5f3f9-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f3f9-128">-Confirm</span></span>
<span data-ttu-id="5f3f9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f3f9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3f9-130">-WhatIf</span></span>
<span data-ttu-id="5f3f9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f3f9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f3f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3f9-133">CommonParameters</span></span>
<span data-ttu-id="5f3f9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f3f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3f9-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f3f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3f9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f3f9-136">INPUTS</span></span>

### <span data-ttu-id="5f3f9-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f3f9-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="5f3f9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5f3f9-138">System.String</span></span>

## <span data-ttu-id="5f3f9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f3f9-139">OUTPUTS</span></span>

### <span data-ttu-id="5f3f9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f3f9-140">System.Boolean</span></span>

## <span data-ttu-id="5f3f9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f3f9-141">NOTES</span></span>

## <span data-ttu-id="5f3f9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f3f9-142">RELATED LINKS</span></span>
