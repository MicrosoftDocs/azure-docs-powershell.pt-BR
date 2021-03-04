---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: 6ccb7b5a38a85d114e3bb93b594d838c61dcff4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888177"
---
# <span data-ttu-id="41733-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="41733-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="41733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41733-102">SYNOPSIS</span></span>
<span data-ttu-id="41733-103">Atualizar um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="41733-103">Update a Data Connector.</span></span>

## <span data-ttu-id="41733-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41733-104">SYNTAX</span></span>

### <span data-ttu-id="41733-105">DataConnectorId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="41733-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41733-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="41733-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41733-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41733-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41733-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41733-108">DESCRIPTION</span></span>
<span data-ttu-id="41733-109">O cmdlet **Update-AzSentinelDataConnector** atualiza o Conector de Dados no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="41733-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="41733-110">Você pode passar um **objeto DataConnector** como um parâmetro ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="41733-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="41733-111">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="41733-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="41733-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41733-112">EXAMPLES</span></span>

### <span data-ttu-id="41733-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41733-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="41733-114">O comando obtém o Conector de Dados *por DataConnectorId* e define o estado *Alertas* como *Desabilitado*.</span><span class="sxs-lookup"><span data-stu-id="41733-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="41733-115">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="41733-115">All other properties remain the same.</span></span>

## <span data-ttu-id="41733-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41733-116">PARAMETERS</span></span>

### <span data-ttu-id="41733-117">-Alerts</span><span class="sxs-lookup"><span data-stu-id="41733-117">-Alerts</span></span>
<span data-ttu-id="41733-118">Alertas do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="41733-119">-AwsRoleArn</span></span>
<span data-ttu-id="41733-120">Função AWS do Conector de Dados Arn</span><span class="sxs-lookup"><span data-stu-id="41733-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="41733-121">-DataConnectorId</span></span>
<span data-ttu-id="41733-122">ID do Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="41733-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41733-123">-DefaultProfile</span></span>
<span data-ttu-id="41733-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41733-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="41733-125">-DiscoveryLogs</span></span>
<span data-ttu-id="41733-126">Logs de Descoberta do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="41733-127">-Exchange</span></span>
<span data-ttu-id="41733-128">Exchange do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-129">-Indicators</span><span class="sxs-lookup"><span data-stu-id="41733-129">-Indicators</span></span>
<span data-ttu-id="41733-130">Indicadores do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41733-131">-InputObject</span></span>
<span data-ttu-id="41733-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="41733-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41733-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="41733-133">-Logs</span></span>
<span data-ttu-id="41733-134">Logs do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41733-135">-ResourceGroupName</span></span>
<span data-ttu-id="41733-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41733-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41733-137">-ResourceId</span></span>
<span data-ttu-id="41733-138">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="41733-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41733-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="41733-139">-SharePoint</span></span>
<span data-ttu-id="41733-140">SharePoint do Conector de Dados</span><span class="sxs-lookup"><span data-stu-id="41733-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41733-141">-SubscriptionId</span></span>
<span data-ttu-id="41733-142">ID de assinatura do conector de dados</span><span class="sxs-lookup"><span data-stu-id="41733-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="41733-143">-WorkspaceName</span></span>
<span data-ttu-id="41733-144">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="41733-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41733-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41733-145">-Confirm</span></span>
<span data-ttu-id="41733-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41733-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41733-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41733-147">-WhatIf</span></span>
<span data-ttu-id="41733-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41733-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41733-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41733-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41733-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41733-150">CommonParameters</span></span>
<span data-ttu-id="41733-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41733-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41733-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41733-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41733-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41733-153">INPUTS</span></span>

### <span data-ttu-id="41733-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="41733-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="41733-155">System.String</span><span class="sxs-lookup"><span data-stu-id="41733-155">System.String</span></span>

## <span data-ttu-id="41733-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41733-156">OUTPUTS</span></span>

### <span data-ttu-id="41733-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="41733-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="41733-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="41733-158">NOTES</span></span>

## <span data-ttu-id="41733-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41733-159">RELATED LINKS</span></span>
