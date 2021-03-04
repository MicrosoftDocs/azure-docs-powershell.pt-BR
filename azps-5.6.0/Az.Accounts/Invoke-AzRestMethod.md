---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: 355de1e4eb4518b8ec3d7291b20f76bda5fb1a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885763"
---
# <span data-ttu-id="7e69a-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="7e69a-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="7e69a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e69a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e69a-103">Construir e executar solicitação HTTP somente para o ponto de extremidade de gerenciamento de recursos do Azure</span><span class="sxs-lookup"><span data-stu-id="7e69a-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="7e69a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e69a-104">SYNTAX</span></span>

### <span data-ttu-id="7e69a-105">ByPath (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7e69a-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e69a-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="7e69a-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e69a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e69a-107">DESCRIPTION</span></span>
<span data-ttu-id="7e69a-108">Construir e executar solicitação HTTP somente para o ponto de extremidade de gerenciamento de recursos do Azure</span><span class="sxs-lookup"><span data-stu-id="7e69a-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="7e69a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e69a-109">EXAMPLES</span></span>

### <span data-ttu-id="7e69a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e69a-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="7e69a-111">Obter espaço de trabalho de análise de log por caminho</span><span class="sxs-lookup"><span data-stu-id="7e69a-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="7e69a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e69a-112">PARAMETERS</span></span>

### <span data-ttu-id="7e69a-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e69a-113">-ApiVersion</span></span>
<span data-ttu-id="7e69a-114">Versão da Api</span><span class="sxs-lookup"><span data-stu-id="7e69a-114">Api Version</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e69a-115">-AsJob</span></span>
<span data-ttu-id="7e69a-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7e69a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e69a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e69a-117">-DefaultProfile</span></span>
<span data-ttu-id="7e69a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e69a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e69a-119">-Method</span><span class="sxs-lookup"><span data-stu-id="7e69a-119">-Method</span></span>
<span data-ttu-id="7e69a-120">Método Http</span><span class="sxs-lookup"><span data-stu-id="7e69a-120">Http Method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e69a-121">-Name</span></span>
<span data-ttu-id="7e69a-122">lista de Nome do Recurso de Destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-122">list of Target Resource Name</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-123">-Path</span><span class="sxs-lookup"><span data-stu-id="7e69a-123">-Path</span></span>
<span data-ttu-id="7e69a-124">Caminho de destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-124">Target Path</span></span>

```yaml
Type: System.String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-125">-Carga</span><span class="sxs-lookup"><span data-stu-id="7e69a-125">-Payload</span></span>
<span data-ttu-id="7e69a-126">Carga de formato JSON</span><span class="sxs-lookup"><span data-stu-id="7e69a-126">JSON format payload</span></span>

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

### <span data-ttu-id="7e69a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e69a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e69a-128">Nome do grupo de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-128">Target Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="7e69a-129">-ResourceProviderName</span></span>
<span data-ttu-id="7e69a-130">Nome do provedor de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-130">Target Resource Provider Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7e69a-131">-ResourceType</span></span>
<span data-ttu-id="7e69a-132">Lista de Tipo de Recurso de Destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-132">List of Target Resource Type</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e69a-133">-SubscriptionId</span></span>
<span data-ttu-id="7e69a-134">ID de assinatura de destino</span><span class="sxs-lookup"><span data-stu-id="7e69a-134">Target Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e69a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e69a-135">-Confirm</span></span>
<span data-ttu-id="7e69a-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e69a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e69a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e69a-137">-WhatIf</span></span>
<span data-ttu-id="7e69a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e69a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e69a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e69a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e69a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e69a-140">CommonParameters</span></span>
<span data-ttu-id="7e69a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e69a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e69a-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e69a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e69a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e69a-143">INPUTS</span></span>

### <span data-ttu-id="7e69a-144">System.string</span><span class="sxs-lookup"><span data-stu-id="7e69a-144">System.string</span></span>

## <span data-ttu-id="7e69a-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e69a-145">OUTPUTS</span></span>

### <span data-ttu-id="7e69a-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="7e69a-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="7e69a-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e69a-147">NOTES</span></span>

## <span data-ttu-id="7e69a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e69a-148">RELATED LINKS</span></span>
