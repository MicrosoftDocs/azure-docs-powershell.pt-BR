---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115115"
---
# <span data-ttu-id="8bdce-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="8bdce-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="8bdce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bdce-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdce-103">Construir e executar solicitação HTTP somente para o ponto de extremidade do Azure Resource Management</span><span class="sxs-lookup"><span data-stu-id="8bdce-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="8bdce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bdce-104">SYNTAX</span></span>

### <span data-ttu-id="8bdce-105">ByPath (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bdce-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdce-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="8bdce-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bdce-107">DESCRIPTION</span></span>
<span data-ttu-id="8bdce-108">Construir e executar solicitação HTTP somente para o ponto de extremidade do Azure Resource Management</span><span class="sxs-lookup"><span data-stu-id="8bdce-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="8bdce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bdce-109">EXAMPLES</span></span>

### <span data-ttu-id="8bdce-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bdce-110">Example 1</span></span>
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

<span data-ttu-id="8bdce-111">Obter espaço de trabalho de análise de log por caminho</span><span class="sxs-lookup"><span data-stu-id="8bdce-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="8bdce-112">OS</span><span class="sxs-lookup"><span data-stu-id="8bdce-112">PARAMETERS</span></span>

### <span data-ttu-id="8bdce-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8bdce-113">-ApiVersion</span></span>
<span data-ttu-id="8bdce-114">Versão da API</span><span class="sxs-lookup"><span data-stu-id="8bdce-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bdce-115">-AsJob</span></span>
<span data-ttu-id="8bdce-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8bdce-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdce-117">-DefaultProfile</span></span>
<span data-ttu-id="8bdce-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdce-119">-Método</span><span class="sxs-lookup"><span data-stu-id="8bdce-119">-Method</span></span>
<span data-ttu-id="8bdce-120">Método http</span><span class="sxs-lookup"><span data-stu-id="8bdce-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bdce-121">-Name</span></span>
<span data-ttu-id="8bdce-122">lista de nome do recurso de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8bdce-123">-Path</span></span>
<span data-ttu-id="8bdce-124">Caminho de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="8bdce-125">-Payload</span></span>
<span data-ttu-id="8bdce-126">Carga de formato JSON</span><span class="sxs-lookup"><span data-stu-id="8bdce-126">JSON format payload</span></span>

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

### <span data-ttu-id="8bdce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdce-127">-ResourceGroupName</span></span>
<span data-ttu-id="8bdce-128">Nome do grupo de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="8bdce-129">-ResourceProviderName</span></span>
<span data-ttu-id="8bdce-130">Nome do provedor de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8bdce-131">-ResourceType</span></span>
<span data-ttu-id="8bdce-132">Lista de tipos de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bdce-133">-SubscriptionId</span></span>
<span data-ttu-id="8bdce-134">ID da assinatura de destino</span><span class="sxs-lookup"><span data-stu-id="8bdce-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdce-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bdce-135">-Confirm</span></span>
<span data-ttu-id="8bdce-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bdce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdce-137">-WhatIf</span></span>
<span data-ttu-id="8bdce-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bdce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdce-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bdce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdce-140">CommonParameters</span></span>
<span data-ttu-id="8bdce-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdce-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bdce-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdce-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bdce-143">INPUTS</span></span>

### <span data-ttu-id="8bdce-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8bdce-144">System.string</span></span>

## <span data-ttu-id="8bdce-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bdce-145">OUTPUTS</span></span>

### <span data-ttu-id="8bdce-146">Microsoft. Azure. Commands. Profile. Models. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="8bdce-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="8bdce-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bdce-147">NOTES</span></span>

## <span data-ttu-id="8bdce-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bdce-148">RELATED LINKS</span></span>
