---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117150"
---
# <span data-ttu-id="578ad-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="578ad-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="578ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="578ad-102">SYNOPSIS</span></span>
<span data-ttu-id="578ad-103">Criar um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="578ad-103">Create a Data Connector.</span></span>

## <span data-ttu-id="578ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="578ad-104">SYNTAX</span></span>

### <span data-ttu-id="578ad-105">AzureActiveDirectory (Padrão)</span><span class="sxs-lookup"><span data-stu-id="578ad-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="578ad-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="578ad-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="578ad-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="578ad-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="578ad-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="578ad-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="578ad-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578ad-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="578ad-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="578ad-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="578ad-113">DESCRIPTION</span></span>
<span data-ttu-id="578ad-114">O cmdlet **New-AzSentinelAlertRule** cria uma Analytic (Regra de Alerta) no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="578ad-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="578ad-115">Você deve especificar um dos parâmetros, por exemplo - AzureActiveDirectory, para especificar o tipo de regra de Alerta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="578ad-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="578ad-116">Cada Tipo tem diferentes paramaters necessários.</span><span class="sxs-lookup"><span data-stu-id="578ad-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="578ad-117">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="578ad-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="578ad-118">Observação: nem todos os conectores de dados disponíveis no portal podem ser disponibilizados por meio da API.</span><span class="sxs-lookup"><span data-stu-id="578ad-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="578ad-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="578ad-119">EXAMPLES</span></span>

### <span data-ttu-id="578ad-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="578ad-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="578ad-121">Este exemplo cria um **DataConnector** para a Central de Segurança do Azure no espaço de trabalho especificado e o armazena na variável $DataConnector dados.</span><span class="sxs-lookup"><span data-stu-id="578ad-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="578ad-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="578ad-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="578ad-123">Este exemplo cria um **DataConnector** para a Segurança do Aplicativo Microsoft Cloud no espaço de trabalho especificado e, em seguida, o armazena na variável $DataConnector dados.</span><span class="sxs-lookup"><span data-stu-id="578ad-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="578ad-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="578ad-124">PARAMETERS</span></span>

### <span data-ttu-id="578ad-125">-Alertas</span><span class="sxs-lookup"><span data-stu-id="578ad-125">-Alerts</span></span>
<span data-ttu-id="578ad-126">Alertas do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="578ad-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="578ad-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="578ad-128">Trilha de Nuvem do Amazon Web Services do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="578ad-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="578ad-129">-AwsRoleArn</span></span>
<span data-ttu-id="578ad-130">Função AWS do Conector de Dados Arn</span><span class="sxs-lookup"><span data-stu-id="578ad-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="578ad-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="578ad-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="578ad-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="578ad-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="578ad-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="578ad-134">Proteção Avançada contra Ameaças do Azure do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="578ad-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="578ad-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="578ad-136">Central de Segurança do Azure do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="578ad-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="578ad-137">-DataConnectorId</span></span>
<span data-ttu-id="578ad-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="578ad-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578ad-139">-DefaultProfile</span></span>
<span data-ttu-id="578ad-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="578ad-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578ad-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="578ad-141">-DiscoveryLogs</span></span>
<span data-ttu-id="578ad-142">Logs de Descoberta do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="578ad-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="578ad-143">-Exchange</span></span>
<span data-ttu-id="578ad-144">Troca de Conectores de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="578ad-145">-Indicadores</span><span class="sxs-lookup"><span data-stu-id="578ad-145">-Indicators</span></span>
<span data-ttu-id="578ad-146">Indicadores do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="578ad-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="578ad-147">-Logs</span></span>
<span data-ttu-id="578ad-148">Logs do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="578ad-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="578ad-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="578ad-150">Segurança do aplicativo Microsoft Cloud Do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="578ad-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="578ad-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="578ad-152">Proteção Avançada contra Ameaças do Microsoft Defender Do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="578ad-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="578ad-153">-Office365</span></span>
<span data-ttu-id="578ad-154">Conector de Dados do Office 365</span><span class="sxs-lookup"><span data-stu-id="578ad-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="578ad-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578ad-155">-ResourceGroupName</span></span>
<span data-ttu-id="578ad-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="578ad-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="578ad-157">-SharePoint</span></span>
<span data-ttu-id="578ad-158">SharePoint do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="578ad-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="578ad-159">-SubscriptionId</span></span>
<span data-ttu-id="578ad-160">ID da assinatura do conector de dados</span><span class="sxs-lookup"><span data-stu-id="578ad-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="578ad-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="578ad-161">-ThreatIntelligence</span></span>
<span data-ttu-id="578ad-162">Inteligência contra Ameaças do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="578ad-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="578ad-163">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="578ad-163">-WorkspaceName</span></span>
<span data-ttu-id="578ad-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="578ad-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="578ad-165">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="578ad-165">-Confirm</span></span>
<span data-ttu-id="578ad-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="578ad-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578ad-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578ad-167">-WhatIf</span></span>
<span data-ttu-id="578ad-168">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="578ad-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="578ad-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="578ad-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578ad-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578ad-170">CommonParameters</span></span>
<span data-ttu-id="578ad-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="578ad-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578ad-172">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="578ad-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578ad-173">Entradas</span><span class="sxs-lookup"><span data-stu-id="578ad-173">INPUTS</span></span>

### <span data-ttu-id="578ad-174">Nenhum</span><span class="sxs-lookup"><span data-stu-id="578ad-174">None</span></span>
## <span data-ttu-id="578ad-175">Saídas</span><span class="sxs-lookup"><span data-stu-id="578ad-175">OUTPUTS</span></span>

### <span data-ttu-id="578ad-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="578ad-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="578ad-177">Notas</span><span class="sxs-lookup"><span data-stu-id="578ad-177">NOTES</span></span>

## <span data-ttu-id="578ad-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="578ad-178">RELATED LINKS</span></span>
