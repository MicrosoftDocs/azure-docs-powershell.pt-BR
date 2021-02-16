---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117579"
---
# <span data-ttu-id="1f703-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f703-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1f703-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f703-102">SYNOPSIS</span></span>
<span data-ttu-id="1f703-103">Cria uma configuração de lote de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="1f703-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f703-104">SYNTAX</span></span>

### <span data-ttu-id="1f703-105">ByIntegrationAccountAndParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f703-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="1f703-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1f703-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="1f703-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1f703-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="1f703-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="1f703-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1f703-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f703-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="1f703-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f703-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f703-114">DESCRIPTION</span></span>
<span data-ttu-id="1f703-115">O **cmdlet Get-AzIntegrationAccountBatchConfiguration** cria uma nova configuração em lotes em uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="1f703-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f703-116">EXAMPLES</span></span>

### <span data-ttu-id="1f703-117">Exemplo 1: Criar nova configuração em lotes usando o arquivo local</span><span class="sxs-lookup"><span data-stu-id="1f703-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1f703-118">Cria uma nova configuração em lotes usando o arquivo local localizado no caminho de arquivo contido em "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="1f703-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="1f703-119">Exemplo 2: Criar nova configuração em lotes usando uma cadeia de caracteres JSON</span><span class="sxs-lookup"><span data-stu-id="1f703-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1f703-120">Cria uma nova configuração de lote usando a cadeia de caracteres JSON contida em "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="1f703-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="1f703-121">Exemplo 3: Criar nova configuração em lotes usando parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f703-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1f703-122">Cria uma nova configuração em lotes fornecendo manualmente todos os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="1f703-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="1f703-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f703-123">PARAMETERS</span></span>

### <span data-ttu-id="1f703-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="1f703-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="1f703-125">A definição de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="1f703-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="1f703-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="1f703-127">O caminho do arquivo de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="1f703-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="1f703-128">-BatchGroupName</span></span>
<span data-ttu-id="1f703-129">O nome do grupo de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="1f703-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="1f703-130">-BatchSize</span></span>
<span data-ttu-id="1f703-131">O tamanho do lote de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="1f703-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f703-132">-DefaultProfile</span></span>
<span data-ttu-id="1f703-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f703-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f703-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="1f703-134">-MessageCount</span></span>
<span data-ttu-id="1f703-135">A contagem de mensagens de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="1f703-136">-Metadados</span><span class="sxs-lookup"><span data-stu-id="1f703-136">-Metadata</span></span>
<span data-ttu-id="1f703-137">Os metadados de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="1f703-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f703-138">-Name</span></span>
<span data-ttu-id="1f703-139">O nome de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="1f703-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="1f703-140">-ParentName</span></span>
<span data-ttu-id="1f703-141">O nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-141">The integration account name.</span></span>

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

### <span data-ttu-id="1f703-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1f703-142">-ParentObject</span></span>
<span data-ttu-id="1f703-143">Um objeto de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-143">An integration account object.</span></span>

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

### <span data-ttu-id="1f703-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1f703-144">-ParentResourceId</span></span>
<span data-ttu-id="1f703-145">A ID do recurso de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="1f703-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f703-146">-ResourceGroupName</span></span>
<span data-ttu-id="1f703-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f703-147">The resource group name.</span></span>

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

### <span data-ttu-id="1f703-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="1f703-148">-ScheduleFrequency</span></span>
<span data-ttu-id="1f703-149">A frequência de agendamento de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="1f703-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="1f703-150">-ScheduleInterval</span></span>
<span data-ttu-id="1f703-151">O intervalo de agendamento de configuração em lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="1f703-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="1f703-152">-ScheduleStartTime</span></span>
<span data-ttu-id="1f703-153">A hora de início do cronograma de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="1f703-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="1f703-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="1f703-155">O fuso horário de configuração de lote da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1f703-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="1f703-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f703-156">-Confirm</span></span>
<span data-ttu-id="1f703-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f703-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f703-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f703-158">-WhatIf</span></span>
<span data-ttu-id="1f703-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f703-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f703-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f703-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f703-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f703-161">CommonParameters</span></span>
<span data-ttu-id="1f703-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f703-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f703-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f703-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f703-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f703-164">INPUTS</span></span>

### <span data-ttu-id="1f703-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1f703-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="1f703-166">System.String</span><span class="sxs-lookup"><span data-stu-id="1f703-166">System.String</span></span>

## <span data-ttu-id="1f703-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f703-167">OUTPUTS</span></span>

### <span data-ttu-id="1f703-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f703-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1f703-169">Notas</span><span class="sxs-lookup"><span data-stu-id="1f703-169">NOTES</span></span>

## <span data-ttu-id="1f703-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f703-170">RELATED LINKS</span></span>
