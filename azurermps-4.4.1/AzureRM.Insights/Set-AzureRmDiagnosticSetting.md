---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603367"
---
# <span data-ttu-id="1a46d-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="1a46d-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="1a46d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a46d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a46d-103">Define as configurações de logs e métricas do recurso.</span><span class="sxs-lookup"><span data-stu-id="1a46d-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a46d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a46d-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a46d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a46d-105">DESCRIPTION</span></span>
<span data-ttu-id="1a46d-106">O cmdlet **set-AzureRmDiagnosticSetting** habilita ou desabilita cada intervalo de tempo e categoria de log para o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="1a46d-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="1a46d-107">Os logs e as métricas são armazenados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="1a46d-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="1a46d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a46d-108">EXAMPLES</span></span>

### <span data-ttu-id="1a46d-109">Exemplo 1: habilitar todas as métricas e registros para um recurso</span><span class="sxs-lookup"><span data-stu-id="1a46d-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="1a46d-110">Esse comando habilita todas as métricas e logs disponíveis para o Resource01.</span><span class="sxs-lookup"><span data-stu-id="1a46d-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="1a46d-111">Exemplo 2: desabilitar todas as métricas e registros</span><span class="sxs-lookup"><span data-stu-id="1a46d-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="1a46d-112">Esse comando desabilita todas as métricas e logs disponíveis para o recurso Resource01.</span><span class="sxs-lookup"><span data-stu-id="1a46d-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="1a46d-113">Exemplo 3: habilitar várias categorias</span><span class="sxs-lookup"><span data-stu-id="1a46d-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

<span data-ttu-id="1a46d-114">Esse comando habilita Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="1a46d-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="1a46d-115">Todas as refinas do timefinas e outras categorias permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="1a46d-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="1a46d-116">Exemplo 4: habilitar um intervalo de tempo e várias categorias</span><span class="sxs-lookup"><span data-stu-id="1a46d-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="1a46d-117">Esse comando habilita somente o Category1, o Category2 e o intervalo de tempo PT1M.</span><span class="sxs-lookup"><span data-stu-id="1a46d-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="1a46d-118">Todas as outras granularidades de tempo e categorias não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="1a46d-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="1a46d-119">OS</span><span class="sxs-lookup"><span data-stu-id="1a46d-119">PARAMETERS</span></span>

### <span data-ttu-id="1a46d-120">-Categorias</span><span class="sxs-lookup"><span data-stu-id="1a46d-120">-Categories</span></span>
<span data-ttu-id="1a46d-121">Especifica a lista de categorias de log para habilitar ou desabilitar, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="1a46d-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="1a46d-122">Se você não especificar uma categoria, esse comando funcionará em todas as categorias.</span><span class="sxs-lookup"><span data-stu-id="1a46d-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-123">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="1a46d-123">-Enabled</span></span>
<span data-ttu-id="1a46d-124">Indica se os diagnósticos devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="1a46d-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="1a46d-125">Especifique $True para habilitar o diagnóstico ou $False para desabilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="1a46d-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a46d-126">-ResourceId</span></span>
<span data-ttu-id="1a46d-127">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1a46d-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="1a46d-128">-RetentionEnabled</span></span>
<span data-ttu-id="1a46d-129">Indica se a retenção de informações de diagnóstico está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1a46d-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1a46d-130">-RetentionInDays</span></span>
<span data-ttu-id="1a46d-131">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="1a46d-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="1a46d-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1a46d-133">-StorageAccountId</span></span>
<span data-ttu-id="1a46d-134">Especifica a ID da conta de armazenamento na qual os dados são salvos.</span><span class="sxs-lookup"><span data-stu-id="1a46d-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-135">-Refinamentos</span><span class="sxs-lookup"><span data-stu-id="1a46d-135">-Timegrains</span></span>
<span data-ttu-id="1a46d-136">Especifica o intervalo de tempo para habilitar ou desabilitar as métricas, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="1a46d-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="1a46d-137">Se você não especificar um intervalo de tempo, esse comando funcionará em todos os refinamentos de tempo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1a46d-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-138">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="1a46d-138">-WorkspaceId</span></span>
<span data-ttu-id="1a46d-139">A ID do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="1a46d-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a46d-140">-DefaultProfile</span></span>
<span data-ttu-id="1a46d-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a46d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="1a46d-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="1a46d-143">A ID da regra do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="1a46d-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a46d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a46d-144">CommonParameters</span></span>
<span data-ttu-id="1a46d-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a46d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a46d-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a46d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a46d-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a46d-147">INPUTS</span></span>

## <span data-ttu-id="1a46d-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a46d-148">OUTPUTS</span></span>

### <span data-ttu-id="1a46d-149">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="1a46d-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="1a46d-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a46d-150">NOTES</span></span>

## <span data-ttu-id="1a46d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a46d-151">RELATED LINKS</span></span>

[<span data-ttu-id="1a46d-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="1a46d-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


