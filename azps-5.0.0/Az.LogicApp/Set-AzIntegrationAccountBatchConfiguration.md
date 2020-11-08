---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126070"
---
# <span data-ttu-id="a5d1b-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d1b-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a5d1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d1b-103">Modifica uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a5d1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d1b-104">SYNTAX</span></span>

### <span data-ttu-id="a5d1b-105">ByIntegrationAccountAndParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5d1b-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="a5d1b-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a5d1b-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="a5d1b-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a5d1b-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="a5d1b-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="a5d1b-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a5d1b-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1b-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="a5d1b-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d1b-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5d1b-114">DESCRIPTION</span></span>
<span data-ttu-id="a5d1b-115">O cmdlet **set-AzIntegrationAccountBatchConfiguration** modifica uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="a5d1b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d1b-116">EXAMPLES</span></span>

### <span data-ttu-id="a5d1b-117">Exemplo 1: modificar uma configuração em lotes usando um arquivo local</span><span class="sxs-lookup"><span data-stu-id="a5d1b-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a5d1b-118">Modifique uma configuração em lotes chamada "sampleBatchConfig" usando o arquivo local localizado no caminho do arquivo contido em "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="a5d1b-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="a5d1b-119">Exemplo 2: modificar uma configuração em lotes usando uma cadeia de caracteres JSON</span><span class="sxs-lookup"><span data-stu-id="a5d1b-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a5d1b-120">Modifique uma configuração em lotes chamada "sampleBatchConfig" usando a cadeia de caracteres JSON contida em "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="a5d1b-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="a5d1b-121">Exemplo 3: modificar uma configuração em lotes usando parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5d1b-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="a5d1b-122">Modifique uma configuração em lotes chamada "sampleBatchConfig" fornecendo manualmente todos os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="a5d1b-123">OS</span><span class="sxs-lookup"><span data-stu-id="a5d1b-123">PARAMETERS</span></span>

### <span data-ttu-id="a5d1b-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="a5d1b-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="a5d1b-125">A definição de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="a5d1b-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="a5d1b-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="a5d1b-127">O caminho do arquivo de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="a5d1b-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d1b-128">-BatchGroupName</span></span>
<span data-ttu-id="a5d1b-129">O nome do grupo de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="a5d1b-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="a5d1b-130">-BatchSize</span></span>
<span data-ttu-id="a5d1b-131">O tamanho do lote de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="a5d1b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d1b-132">-DefaultProfile</span></span>
<span data-ttu-id="a5d1b-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d1b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d1b-134">-InputObject</span></span>
<span data-ttu-id="a5d1b-135">Uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="a5d1b-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="a5d1b-136">-MessageCount</span></span>
<span data-ttu-id="a5d1b-137">A contagem de mensagens de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="a5d1b-138">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a5d1b-138">-Metadata</span></span>
<span data-ttu-id="a5d1b-139">Metadados de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="a5d1b-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5d1b-140">-Name</span></span>
<span data-ttu-id="a5d1b-141">O nome de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="a5d1b-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a5d1b-142">-ParentName</span></span>
<span data-ttu-id="a5d1b-143">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-143">The integration account name.</span></span>

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

### <span data-ttu-id="a5d1b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d1b-144">-ResourceGroupName</span></span>
<span data-ttu-id="a5d1b-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-145">The resource group name.</span></span>

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

### <span data-ttu-id="a5d1b-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d1b-146">-ResourceId</span></span>
<span data-ttu-id="a5d1b-147">A ID do recurso de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="a5d1b-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="a5d1b-148">-ScheduleFrequency</span></span>
<span data-ttu-id="a5d1b-149">A frequência de agendamento da configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="a5d1b-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="a5d1b-150">-ScheduleInterval</span></span>
<span data-ttu-id="a5d1b-151">O intervalo de agendamento de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="a5d1b-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="a5d1b-152">-ScheduleStartTime</span></span>
<span data-ttu-id="a5d1b-153">A hora de início da agenda de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="a5d1b-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="a5d1b-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="a5d1b-155">O fuso horário da agenda de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="a5d1b-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5d1b-156">-Confirm</span></span>
<span data-ttu-id="a5d1b-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d1b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d1b-158">-WhatIf</span></span>
<span data-ttu-id="a5d1b-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5d1b-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d1b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d1b-161">CommonParameters</span></span>
<span data-ttu-id="a5d1b-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d1b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d1b-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d1b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d1b-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5d1b-164">INPUTS</span></span>

### <span data-ttu-id="a5d1b-165">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d1b-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="a5d1b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d1b-166">System.String</span></span>

## <span data-ttu-id="a5d1b-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5d1b-167">OUTPUTS</span></span>

### <span data-ttu-id="a5d1b-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d1b-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="a5d1b-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5d1b-169">NOTES</span></span>

## <span data-ttu-id="a5d1b-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d1b-170">RELATED LINKS</span></span>
