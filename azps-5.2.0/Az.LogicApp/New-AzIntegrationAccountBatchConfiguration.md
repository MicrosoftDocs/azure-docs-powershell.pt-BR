---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263142"
---
# <span data-ttu-id="544d7-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="544d7-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="544d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="544d7-102">SYNOPSIS</span></span>
<span data-ttu-id="544d7-103">Cria uma configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="544d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="544d7-104">SYNTAX</span></span>

### <span data-ttu-id="544d7-105">ByIntegrationAccountAndParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="544d7-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="544d7-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="544d7-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="544d7-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="544d7-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="544d7-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="544d7-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="544d7-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544d7-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="544d7-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544d7-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="544d7-114">DESCRIPTION</span></span>
<span data-ttu-id="544d7-115">O cmdlet **Get-AzIntegrationAccountBatchConfiguration** cria uma nova configuração em lotes em uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="544d7-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="544d7-116">EXAMPLES</span></span>

### <span data-ttu-id="544d7-117">Exemplo 1: criar uma nova configuração em lotes usando um arquivo local</span><span class="sxs-lookup"><span data-stu-id="544d7-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="544d7-118">Cria uma nova configuração em lotes usando o arquivo local localizado no caminho do arquivo contido em "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="544d7-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="544d7-119">Exemplo 2: criar uma nova configuração em lotes usando uma cadeia de caracteres JSON</span><span class="sxs-lookup"><span data-stu-id="544d7-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="544d7-120">Cria uma nova configuração em lotes usando a cadeia de caracteres JSON contida em "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="544d7-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="544d7-121">Exemplo 3: criar uma nova configuração em lotes usando parâmetros</span><span class="sxs-lookup"><span data-stu-id="544d7-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="544d7-122">Cria uma nova configuração em lotes fornecendo manualmente todos os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="544d7-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="544d7-123">OS</span><span class="sxs-lookup"><span data-stu-id="544d7-123">PARAMETERS</span></span>

### <span data-ttu-id="544d7-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="544d7-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="544d7-125">A definição de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="544d7-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="544d7-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="544d7-127">O caminho do arquivo de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="544d7-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="544d7-128">-BatchGroupName</span></span>
<span data-ttu-id="544d7-129">O nome do grupo de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="544d7-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="544d7-130">-BatchSize</span></span>
<span data-ttu-id="544d7-131">O tamanho do lote de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="544d7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544d7-132">-DefaultProfile</span></span>
<span data-ttu-id="544d7-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="544d7-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="544d7-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="544d7-134">-MessageCount</span></span>
<span data-ttu-id="544d7-135">A contagem de mensagens de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="544d7-136">-Metadados</span><span class="sxs-lookup"><span data-stu-id="544d7-136">-Metadata</span></span>
<span data-ttu-id="544d7-137">Metadados de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="544d7-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="544d7-138">-Name</span></span>
<span data-ttu-id="544d7-139">O nome de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="544d7-140">-ParentName</span></span>
<span data-ttu-id="544d7-141">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-141">The integration account name.</span></span>

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

### <span data-ttu-id="544d7-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="544d7-142">-ParentObject</span></span>
<span data-ttu-id="544d7-143">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="544d7-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="544d7-144">-ParentResourceId</span></span>
<span data-ttu-id="544d7-145">A ID do recurso de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="544d7-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="544d7-146">-ResourceGroupName</span></span>
<span data-ttu-id="544d7-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="544d7-147">The resource group name.</span></span>

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

### <span data-ttu-id="544d7-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="544d7-148">-ScheduleFrequency</span></span>
<span data-ttu-id="544d7-149">A frequência de agendamento da configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="544d7-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="544d7-150">-ScheduleInterval</span></span>
<span data-ttu-id="544d7-151">O intervalo de agendamento de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="544d7-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="544d7-152">-ScheduleStartTime</span></span>
<span data-ttu-id="544d7-153">A hora de início da agenda de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="544d7-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="544d7-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="544d7-155">O fuso horário da agenda de configuração em lotes da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="544d7-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="544d7-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="544d7-156">-Confirm</span></span>
<span data-ttu-id="544d7-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="544d7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544d7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544d7-158">-WhatIf</span></span>
<span data-ttu-id="544d7-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="544d7-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="544d7-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="544d7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="544d7-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544d7-161">CommonParameters</span></span>
<span data-ttu-id="544d7-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544d7-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544d7-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="544d7-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544d7-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="544d7-164">INPUTS</span></span>

### <span data-ttu-id="544d7-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="544d7-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="544d7-166">System. String</span><span class="sxs-lookup"><span data-stu-id="544d7-166">System.String</span></span>

## <span data-ttu-id="544d7-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="544d7-167">OUTPUTS</span></span>

### <span data-ttu-id="544d7-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="544d7-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="544d7-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="544d7-169">NOTES</span></span>

## <span data-ttu-id="544d7-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="544d7-170">RELATED LINKS</span></span>
