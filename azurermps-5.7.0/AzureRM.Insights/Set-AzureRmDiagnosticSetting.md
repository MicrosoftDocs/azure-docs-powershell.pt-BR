---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427553"
---
# <span data-ttu-id="7a1f3-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7a1f3-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="7a1f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1f3-103">Define as configurações de logs e métricas do recurso.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a1f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a1f3-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a1f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1f3-106">O cmdlet **set-AzureRmDiagnosticSetting** habilita ou desabilita cada intervalo de tempo e categoria de log para o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="7a1f3-107">Os logs e as métricas são armazenados na conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-107">The logs and metrics are stored in the specified storage account.</span></span>

<span data-ttu-id="7a1f3-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7a1f3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a1f3-109">EXAMPLES</span></span>

### <span data-ttu-id="7a1f3-110">Exemplo 1: habilitar todas as métricas e registros para um recurso</span><span class="sxs-lookup"><span data-stu-id="7a1f3-110">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="7a1f3-111">Esse comando habilita todas as métricas e logs disponíveis para o Resource01.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-111">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="7a1f3-112">Exemplo 2: desabilitar todas as métricas e registros</span><span class="sxs-lookup"><span data-stu-id="7a1f3-112">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="7a1f3-113">Esse comando desabilita todas as métricas e logs disponíveis para o recurso Resource01.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-113">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="7a1f3-114">Exemplo 3: habilitar várias categorias</span><span class="sxs-lookup"><span data-stu-id="7a1f3-114">Example 3: Enable multiple categories</span></span>
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

<span data-ttu-id="7a1f3-115">Esse comando habilita Category1 e Category2.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-115">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="7a1f3-116">Todas as refinas do timefinas e outras categorias permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-116">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="7a1f3-117">Exemplo 4: habilitar um intervalo de tempo e várias categorias</span><span class="sxs-lookup"><span data-stu-id="7a1f3-117">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="7a1f3-118">Esse comando habilita somente o Category1, o Category2 e o intervalo de tempo PT1M.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-118">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="7a1f3-119">Todas as outras granularidades de tempo e categorias não são alteradas.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-119">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="7a1f3-120">OS</span><span class="sxs-lookup"><span data-stu-id="7a1f3-120">PARAMETERS</span></span>

### <span data-ttu-id="7a1f3-121">-Categorias</span><span class="sxs-lookup"><span data-stu-id="7a1f3-121">-Categories</span></span>
<span data-ttu-id="7a1f3-122">Especifica a lista de categorias de log para habilitar ou desabilitar, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-122">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="7a1f3-123">Se você não especificar uma categoria, esse comando funcionará em todas as categorias.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-123">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="7a1f3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1f3-124">-DefaultProfile</span></span>
<span data-ttu-id="7a1f3-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7a1f3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-126">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="7a1f3-126">-Enabled</span></span>
<span data-ttu-id="7a1f3-127">Indica se os diagnósticos devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-127">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="7a1f3-128">Especifique $True para habilitar o diagnóstico ou $False para desabilitar o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-128">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-129">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="7a1f3-129">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="7a1f3-130">A regra de Hub de eventos que eu</span><span class="sxs-lookup"><span data-stu-id="7a1f3-130">The event hub rule i</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a1f3-131">-ResourceId</span></span>
<span data-ttu-id="7a1f3-132">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-132">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-133">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="7a1f3-133">-RetentionEnabled</span></span>
<span data-ttu-id="7a1f3-134">Indica se a retenção de informações de diagnóstico está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-134">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7a1f3-135">-RetentionInDays</span></span>
<span data-ttu-id="7a1f3-136">Especifica a política de retenção, em dias.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-136">Specifies the retention policy, in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-137">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="7a1f3-137">-ServiceBusRuleId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7a1f3-138">-StorageAccountId</span></span>
<span data-ttu-id="7a1f3-139">Especifica a ID da conta de armazenamento na qual os dados são salvos.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-139">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-140">-Refinamentos</span><span class="sxs-lookup"><span data-stu-id="7a1f3-140">-Timegrains</span></span>
<span data-ttu-id="7a1f3-141">Especifica o intervalo de tempo para habilitar ou desabilitar as métricas, de acordo com o valor de *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-141">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="7a1f3-142">Se você não especificar um intervalo de tempo, esse comando funcionará em todos os refinamentos de tempo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-142">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="7a1f3-143">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="7a1f3-143">-WorkspaceId</span></span>
<span data-ttu-id="7a1f3-144">A ID do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="7a1f3-144">The Id of the workspace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1f3-145">CommonParameters</span></span>
<span data-ttu-id="7a1f3-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1f3-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1f3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1f3-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a1f3-148">INPUTS</span></span>

### <span data-ttu-id="7a1f3-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a1f3-149">None</span></span>
<span data-ttu-id="7a1f3-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7a1f3-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a1f3-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a1f3-151">OUTPUTS</span></span>

### <span data-ttu-id="7a1f3-152">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="7a1f3-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="7a1f3-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a1f3-153">NOTES</span></span>

## <span data-ttu-id="7a1f3-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a1f3-154">RELATED LINKS</span></span>

[<span data-ttu-id="7a1f3-155">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7a1f3-155">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


