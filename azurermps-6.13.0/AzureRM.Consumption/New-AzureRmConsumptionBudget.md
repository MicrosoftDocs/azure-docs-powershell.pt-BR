---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/new-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
ms.openlocfilehash: 9c89a4791b4e32637d069a672ddde06862518332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433286"
---
# <span data-ttu-id="a1b61-101">New-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="a1b61-101">New-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="a1b61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1b61-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b61-103">Crie um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1b61-103">Create a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1b61-104">SYNTAX</span></span>

### <span data-ttu-id="a1b61-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1b61-105">Subscription (Default)</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b61-106">Forma</span><span class="sxs-lookup"><span data-stu-id="a1b61-106">Notification</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1b61-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b61-108">O cmdlet New-AzureRmConsumptionBudget cria um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1b61-108">The New-AzureRmConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a1b61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1b61-109">EXAMPLES</span></span>

### <span data-ttu-id="a1b61-110">Exemplo 1: criar um orçamento de custo com um nome de orçamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="a1b61-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="a1b61-111">Exemplo 2: criar um orçamento de custo com um nome de orçamento em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a1b61-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="a1b61-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1b61-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b61-113">-Valor</span><span class="sxs-lookup"><span data-stu-id="a1b61-113">-Amount</span></span>
<span data-ttu-id="a1b61-114">Valor de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="a1b61-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-115">-Categoria</span><span class="sxs-lookup"><span data-stu-id="a1b61-115">-Category</span></span>
<span data-ttu-id="a1b61-116">Categoria do orçamento pode ser custo ou uso.</span><span class="sxs-lookup"><span data-stu-id="a1b61-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="a1b61-117">-ContactEmail</span></span>
<span data-ttu-id="a1b61-118">Endereços de email para enviar a notificação de orçamento para quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="a1b61-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-119">-Pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="a1b61-119">-ContactGroup</span></span>
<span data-ttu-id="a1b61-120">Grupos de ações para os quais enviar a notificação de orçamento quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="a1b61-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="a1b61-121">-ContactRole</span></span>
<span data-ttu-id="a1b61-122">Funções de contato para enviar a notificação de orçamento para quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="a1b61-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b61-123">-DefaultProfile</span></span>
<span data-ttu-id="a1b61-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b61-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b61-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a1b61-125">-EndDate</span></span>
<span data-ttu-id="a1b61-126">Data de término (AAAA-MM-DD em UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="a1b61-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="a1b61-127">-MeterFilter</span></span>
<span data-ttu-id="a1b61-128">Lista separada por vírgula de medidores para filtrar.</span><span class="sxs-lookup"><span data-stu-id="a1b61-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="a1b61-129">Obrigatório se a categoria for o uso.</span><span class="sxs-lookup"><span data-stu-id="a1b61-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b61-130">-Name</span></span>
<span data-ttu-id="a1b61-131">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="a1b61-131">Name of a budget.</span></span>

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

### <span data-ttu-id="a1b61-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="a1b61-132">-NotificationEnabled</span></span>
<span data-ttu-id="a1b61-133">A notificação está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="a1b61-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="a1b61-134">-NotificationKey</span></span>
<span data-ttu-id="a1b61-135">Chave de uma notificação associada a um orçamento, necessária para criar uma notificação com uma chave habilitada para notificação, um limite de notificação, emails de contato, grupos de contatos ou funções de contato.</span><span class="sxs-lookup"><span data-stu-id="a1b61-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="a1b61-136">-NotificationThreshold</span></span>
<span data-ttu-id="a1b61-137">Valor limite associado a uma notificação.</span><span class="sxs-lookup"><span data-stu-id="a1b61-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="a1b61-138">A notificação é enviada quando o custo ou o uso excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="a1b61-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="a1b61-139">É sempre porcentagem e deve estar entre 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="a1b61-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="a1b61-140">-ResourceFilter</span></span>
<span data-ttu-id="a1b61-141">Lista separada por vírgula de instâncias de recurso para filtrar.</span><span class="sxs-lookup"><span data-stu-id="a1b61-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="a1b61-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="a1b61-143">Lista separada por vírgula de grupos de recursos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="a1b61-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b61-144">-ResourceGroupName</span></span>
<span data-ttu-id="a1b61-145">Grupo de recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="a1b61-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="a1b61-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a1b61-146">-StartDate</span></span>
<span data-ttu-id="a1b61-147">Data de início (AAAA-MM-DD em UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="a1b61-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="a1b61-148">Não antes do mês atual para o intervalo de tempo mensal.</span><span class="sxs-lookup"><span data-stu-id="a1b61-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="a1b61-149">Não antes de três meses para o intervalo trimestral de tempo.</span><span class="sxs-lookup"><span data-stu-id="a1b61-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="a1b61-150">Não antes de 12 meses por um intervalo de tempo anual.</span><span class="sxs-lookup"><span data-stu-id="a1b61-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="a1b61-151">Data de início futuro não tem mais de três meses.</span><span class="sxs-lookup"><span data-stu-id="a1b61-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-152">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="a1b61-152">-TimeGrain</span></span>
<span data-ttu-id="a1b61-153">O intervalo de tempo do orçamento pode ser mensal, trimestral ou anualmente.</span><span class="sxs-lookup"><span data-stu-id="a1b61-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b61-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1b61-154">-Confirm</span></span>
<span data-ttu-id="a1b61-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b61-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b61-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b61-156">-WhatIf</span></span>
<span data-ttu-id="a1b61-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1b61-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b61-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1b61-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b61-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b61-159">CommonParameters</span></span>
<span data-ttu-id="a1b61-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b61-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b61-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b61-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b61-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1b61-162">INPUTS</span></span>

### <span data-ttu-id="a1b61-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1b61-163">None</span></span>

## <span data-ttu-id="a1b61-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1b61-164">OUTPUTS</span></span>

### <span data-ttu-id="a1b61-165">Microsoft. Azure. Commands. consumo. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="a1b61-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="a1b61-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1b61-166">NOTES</span></span>

## <span data-ttu-id="a1b61-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1b61-167">RELATED LINKS</span></span>
