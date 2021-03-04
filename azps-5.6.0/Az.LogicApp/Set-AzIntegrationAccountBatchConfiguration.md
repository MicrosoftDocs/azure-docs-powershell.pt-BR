---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887980"
---
# <span data-ttu-id="ff482-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff482-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="ff482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff482-102">SYNOPSIS</span></span>
<span data-ttu-id="ff482-103">Modifica uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="ff482-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ff482-104">SYNTAX</span></span>

### <span data-ttu-id="ff482-105">ByIntegrationAccountAndParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ff482-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="ff482-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff482-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="ff482-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff482-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="ff482-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="ff482-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="ff482-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff482-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="ff482-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff482-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ff482-114">DESCRIPTION</span></span>
<span data-ttu-id="ff482-115">O cmdlet **Set-AzIntegrationAccountBatchConfiguration** modifica uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="ff482-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff482-116">EXAMPLES</span></span>

### <span data-ttu-id="ff482-117">Exemplo 1: Modificar uma configuração em lote usando o arquivo local</span><span class="sxs-lookup"><span data-stu-id="ff482-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff482-118">Modifique uma configuração em lote chamada "sampleBatchConfig" usando o arquivo local localizado no caminho do arquivo contido em "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="ff482-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="ff482-119">Exemplo 2: Modificar uma configuração em lote usando uma cadeia de caracteres JSON</span><span class="sxs-lookup"><span data-stu-id="ff482-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff482-120">Modifique uma configuração em lote chamada "sampleBatchConfig" usando a cadeia de caracteres JSON contida em "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="ff482-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="ff482-121">Exemplo 3: Modificar uma configuração em lote usando parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff482-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="ff482-122">Modifique uma configuração em lote chamada "sampleBatchConfig" fornecendo manualmente todos os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="ff482-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="ff482-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ff482-123">PARAMETERS</span></span>

### <span data-ttu-id="ff482-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="ff482-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="ff482-125">A definição de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="ff482-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="ff482-127">O caminho do arquivo de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="ff482-128">-BatchGroupName</span></span>
<span data-ttu-id="ff482-129">O nome do grupo de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="ff482-130">-BatchSize</span></span>
<span data-ttu-id="ff482-131">O tamanho do lote de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff482-132">-DefaultProfile</span></span>
<span data-ttu-id="ff482-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff482-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff482-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff482-134">-InputObject</span></span>
<span data-ttu-id="ff482-135">Uma configuração em lotes de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="ff482-136">-MessageCount</span></span>
<span data-ttu-id="ff482-137">A contagem de mensagens de configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-138">-Metadados</span><span class="sxs-lookup"><span data-stu-id="ff482-138">-Metadata</span></span>
<span data-ttu-id="ff482-139">Os metadados de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-140">-Name</span><span class="sxs-lookup"><span data-stu-id="ff482-140">-Name</span></span>
<span data-ttu-id="ff482-141">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="ff482-142">-ParentName</span></span>
<span data-ttu-id="ff482-143">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff482-144">-ResourceGroupName</span></span>
<span data-ttu-id="ff482-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff482-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff482-146">-ResourceId</span></span>
<span data-ttu-id="ff482-147">A ID do recurso de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="ff482-148">-ScheduleFrequency</span></span>
<span data-ttu-id="ff482-149">A frequência de agendamento de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="ff482-150">-ScheduleInterval</span></span>
<span data-ttu-id="ff482-151">O intervalo de agendamento de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="ff482-152">-ScheduleStartTime</span></span>
<span data-ttu-id="ff482-153">A hora de início do cronograma de configuração do lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="ff482-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="ff482-155">O fuso horário de configuração do lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ff482-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff482-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff482-156">-Confirm</span></span>
<span data-ttu-id="ff482-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff482-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff482-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff482-158">-WhatIf</span></span>
<span data-ttu-id="ff482-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff482-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff482-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff482-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff482-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff482-161">CommonParameters</span></span>
<span data-ttu-id="ff482-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff482-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff482-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff482-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff482-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff482-164">INPUTS</span></span>

### <span data-ttu-id="ff482-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff482-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="ff482-166">System.String</span><span class="sxs-lookup"><span data-stu-id="ff482-166">System.String</span></span>

## <span data-ttu-id="ff482-167">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ff482-167">OUTPUTS</span></span>

### <span data-ttu-id="ff482-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff482-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="ff482-169">NOTES</span><span class="sxs-lookup"><span data-stu-id="ff482-169">NOTES</span></span>

## <span data-ttu-id="ff482-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff482-170">RELATED LINKS</span></span>
