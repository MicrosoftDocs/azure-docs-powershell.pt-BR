---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433203"
---
# <span data-ttu-id="88ff6-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="88ff6-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="88ff6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="88ff6-103">Crie um conector de dados.</span><span class="sxs-lookup"><span data-stu-id="88ff6-103">Create a Data Connector.</span></span>

## <span data-ttu-id="88ff6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88ff6-104">SYNTAX</span></span>

### <span data-ttu-id="88ff6-105">AzureActiveDirectory (padrão)</span><span class="sxs-lookup"><span data-stu-id="88ff6-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88ff6-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="88ff6-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="88ff6-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="88ff6-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="88ff6-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="88ff6-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-111">Office365</span><span class="sxs-lookup"><span data-stu-id="88ff6-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff6-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="88ff6-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88ff6-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88ff6-113">DESCRIPTION</span></span>
<span data-ttu-id="88ff6-114">O cmdlet **New-AzSentinelAlertRule** cria uma análise (regra de alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="88ff6-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="88ff6-115">Você deve especificar um dos parâmetros, por exemplo, AzureActiveDirectory, para especificar o tipo de regra de alerta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="88ff6-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="88ff6-116">Cada tipo tem parâmetros obrigatórios diferentes.</span><span class="sxs-lookup"><span data-stu-id="88ff6-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="88ff6-117">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="88ff6-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="88ff6-118">Observação: nem todos os conectores de dados disponíveis no portal são avaialble via API.</span><span class="sxs-lookup"><span data-stu-id="88ff6-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="88ff6-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88ff6-119">EXAMPLES</span></span>

### <span data-ttu-id="88ff6-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88ff6-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="88ff6-121">Este exemplo cria uma central de segurança do **DataConnect** para o Azure no espaço de trabalho especificado e armazena-a na variável $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="88ff6-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="88ff6-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="88ff6-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="88ff6-123">Este exemplo cria um **Dataconnecter** para Microsoft Cloud app Security no espaço de trabalho especificado e, em seguida, armazena-o na variável $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="88ff6-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="88ff6-124">OS</span><span class="sxs-lookup"><span data-stu-id="88ff6-124">PARAMETERS</span></span>

### <span data-ttu-id="88ff6-125">-Alertas</span><span class="sxs-lookup"><span data-stu-id="88ff6-125">-Alerts</span></span>
<span data-ttu-id="88ff6-126">Alertas do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="88ff6-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="88ff6-128">Trail na nuvem de serviços Web do Amazon conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="88ff6-129">-AwsRoleArn</span></span>
<span data-ttu-id="88ff6-130">ARN de função AWS do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="88ff6-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="88ff6-132">Active Directory do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="88ff6-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="88ff6-134">Proteção avançada contra ameaças do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="88ff6-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="88ff6-136">Central de segurança do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-137">-Dataconnectorid</span><span class="sxs-lookup"><span data-stu-id="88ff6-137">-DataConnectorId</span></span>
<span data-ttu-id="88ff6-138">Active Directory do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ff6-139">-DefaultProfile</span></span>
<span data-ttu-id="88ff6-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88ff6-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ff6-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="88ff6-141">-DiscoveryLogs</span></span>
<span data-ttu-id="88ff6-142">Logs de descoberta do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="88ff6-143">-Exchange</span></span>
<span data-ttu-id="88ff6-144">Exchange do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-145">-Indicadores</span><span class="sxs-lookup"><span data-stu-id="88ff6-145">-Indicators</span></span>
<span data-ttu-id="88ff6-146">Indicadores do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="88ff6-147">-Logs</span></span>
<span data-ttu-id="88ff6-148">Logs do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="88ff6-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="88ff6-150">Conector de dados Microsoft Cloud app Security</span><span class="sxs-lookup"><span data-stu-id="88ff6-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="88ff6-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="88ff6-152">Conector de dados proteção avançada contra ameaças Microsoft defender</span><span class="sxs-lookup"><span data-stu-id="88ff6-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="88ff6-153">-Office365</span></span>
<span data-ttu-id="88ff6-154">Conector de dados do Office 365</span><span class="sxs-lookup"><span data-stu-id="88ff6-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ff6-155">-ResourceGroupName</span></span>
<span data-ttu-id="88ff6-156">Active Directory do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-156">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="88ff6-157">-SharePoint</span></span>
<span data-ttu-id="88ff6-158">SharePoint do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88ff6-159">-SubscriptionId</span></span>
<span data-ttu-id="88ff6-160">ID da assinatura do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="88ff6-161">-ThreatIntelligence</span></span>
<span data-ttu-id="88ff6-162">Inteligência de ameaças do conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88ff6-163">-WorkspaceName</span></span>
<span data-ttu-id="88ff6-164">Active Directory do Azure conector de dados</span><span class="sxs-lookup"><span data-stu-id="88ff6-164">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff6-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88ff6-165">-Confirm</span></span>
<span data-ttu-id="88ff6-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88ff6-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ff6-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ff6-167">-WhatIf</span></span>
<span data-ttu-id="88ff6-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88ff6-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88ff6-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88ff6-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ff6-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ff6-170">CommonParameters</span></span>
<span data-ttu-id="88ff6-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ff6-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ff6-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ff6-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ff6-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88ff6-173">INPUTS</span></span>

### <span data-ttu-id="88ff6-174">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88ff6-174">None</span></span>
## <span data-ttu-id="88ff6-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88ff6-175">OUTPUTS</span></span>

### <span data-ttu-id="88ff6-176">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="88ff6-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="88ff6-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88ff6-177">NOTES</span></span>

## <span data-ttu-id="88ff6-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88ff6-178">RELATED LINKS</span></span>
