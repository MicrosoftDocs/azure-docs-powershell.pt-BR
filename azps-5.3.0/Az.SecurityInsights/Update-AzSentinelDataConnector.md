---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433178"
---
# <span data-ttu-id="1e1d4-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1e1d4-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="1e1d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1d4-103">Atualizar um conector de dados.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-103">Update a Data Connector.</span></span>

## <span data-ttu-id="1e1d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e1d4-104">SYNTAX</span></span>

### <span data-ttu-id="1e1d4-105">Dataconnectorid (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e1d4-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1d4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1d4-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1d4-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="1e1d4-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e1d4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e1d4-108">DESCRIPTION</span></span>
<span data-ttu-id="1e1d4-109">O cmdlet **Update-AzSentinelDataConnector** atualiza o conector de dados no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="1e1d4-110">Você pode passar um objeto **DataConnect** como um parâmetro ou usar o operador pipeline ou, como alternativa, pode especificar os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="1e1d4-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1e1d4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e1d4-112">EXAMPLES</span></span>

### <span data-ttu-id="1e1d4-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e1d4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="1e1d4-114">O comando obtém o conector de dados por *Dataconnectorid* e define o estado de *alertas* como *desabilitado*.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="1e1d4-115">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-115">All other properties remain the same.</span></span>

## <span data-ttu-id="1e1d4-116">OS</span><span class="sxs-lookup"><span data-stu-id="1e1d4-116">PARAMETERS</span></span>

### <span data-ttu-id="1e1d4-117">-Alertas</span><span class="sxs-lookup"><span data-stu-id="1e1d4-117">-Alerts</span></span>
<span data-ttu-id="1e1d4-118">Alertas do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-118">Data Connector Alerts</span></span>

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

### <span data-ttu-id="1e1d4-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="1e1d4-119">-AwsRoleArn</span></span>
<span data-ttu-id="1e1d4-120">ARN de função AWS do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-120">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="1e1d4-121">-Dataconnectorid</span><span class="sxs-lookup"><span data-stu-id="1e1d4-121">-DataConnectorId</span></span>
<span data-ttu-id="1e1d4-122">ID do conector de dados.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-122">Data Connector Id.</span></span>

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

### <span data-ttu-id="1e1d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1d4-123">-DefaultProfile</span></span>
<span data-ttu-id="1e1d4-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e1d4-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="1e1d4-125">-DiscoveryLogs</span></span>
<span data-ttu-id="1e1d4-126">Logs de descoberta do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-126">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="1e1d4-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="1e1d4-127">-Exchange</span></span>
<span data-ttu-id="1e1d4-128">Exchange do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-128">Data Connector Exchange</span></span>

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

### <span data-ttu-id="1e1d4-129">-Indicadores</span><span class="sxs-lookup"><span data-stu-id="1e1d4-129">-Indicators</span></span>
<span data-ttu-id="1e1d4-130">Indicadores do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-130">Data Connector Indicators</span></span>

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

### <span data-ttu-id="1e1d4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e1d4-131">-InputObject</span></span>
<span data-ttu-id="1e1d4-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-132">InputObject.</span></span>

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

### <span data-ttu-id="1e1d4-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="1e1d4-133">-Logs</span></span>
<span data-ttu-id="1e1d4-134">Logs do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-134">Data Connector Logs</span></span>

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

### <span data-ttu-id="1e1d4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1d4-135">-ResourceGroupName</span></span>
<span data-ttu-id="1e1d4-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-136">Resource group name.</span></span>

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

### <span data-ttu-id="1e1d4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e1d4-137">-ResourceId</span></span>
<span data-ttu-id="1e1d4-138">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-138">Resource Id.</span></span>

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

### <span data-ttu-id="1e1d4-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="1e1d4-139">-SharePoint</span></span>
<span data-ttu-id="1e1d4-140">SharePoint do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-140">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="1e1d4-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e1d4-141">-SubscriptionId</span></span>
<span data-ttu-id="1e1d4-142">ID da assinatura do conector de dados</span><span class="sxs-lookup"><span data-stu-id="1e1d4-142">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="1e1d4-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e1d4-143">-WorkspaceName</span></span>
<span data-ttu-id="1e1d4-144">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-144">Workspace Name.</span></span>

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

### <span data-ttu-id="1e1d4-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e1d4-145">-Confirm</span></span>
<span data-ttu-id="1e1d4-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e1d4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e1d4-147">-WhatIf</span></span>
<span data-ttu-id="1e1d4-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e1d4-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e1d4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1d4-150">CommonParameters</span></span>
<span data-ttu-id="1e1d4-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1d4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1d4-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e1d4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1d4-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e1d4-153">INPUTS</span></span>

### <span data-ttu-id="1e1d4-154">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1e1d4-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="1e1d4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1e1d4-155">System.String</span></span>

## <span data-ttu-id="1e1d4-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e1d4-156">OUTPUTS</span></span>

### <span data-ttu-id="1e1d4-157">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1e1d4-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="1e1d4-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e1d4-158">NOTES</span></span>

## <span data-ttu-id="1e1d4-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e1d4-159">RELATED LINKS</span></span>
