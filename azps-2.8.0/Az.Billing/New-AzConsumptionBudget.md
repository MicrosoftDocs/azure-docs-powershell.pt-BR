---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 45e41da30d90041c1e8670ebe8e356688785e355
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597653"
---
# <span data-ttu-id="70ae1-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="70ae1-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="70ae1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="70ae1-103">Crie um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70ae1-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="70ae1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70ae1-104">SYNTAX</span></span>

### <span data-ttu-id="70ae1-105">Assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="70ae1-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae1-106">Forma</span><span class="sxs-lookup"><span data-stu-id="70ae1-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ae1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70ae1-107">DESCRIPTION</span></span>
<span data-ttu-id="70ae1-108">O cmdlet New-AzConsumptionBudget cria um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70ae1-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="70ae1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70ae1-109">EXAMPLES</span></span>

### <span data-ttu-id="70ae1-110">Exemplo 1: criar um orçamento de custo com um nome de orçamento no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="70ae1-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="70ae1-111">Exemplo 2: criar um orçamento de custo com um nome de orçamento em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="70ae1-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="70ae1-112">OS</span><span class="sxs-lookup"><span data-stu-id="70ae1-112">PARAMETERS</span></span>

### <span data-ttu-id="70ae1-113">-Valor</span><span class="sxs-lookup"><span data-stu-id="70ae1-113">-Amount</span></span>
<span data-ttu-id="70ae1-114">Valor de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="70ae1-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="70ae1-115">-Categoria</span><span class="sxs-lookup"><span data-stu-id="70ae1-115">-Category</span></span>
<span data-ttu-id="70ae1-116">Categoria do orçamento pode ser custo ou uso.</span><span class="sxs-lookup"><span data-stu-id="70ae1-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="70ae1-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="70ae1-117">-ContactEmail</span></span>
<span data-ttu-id="70ae1-118">Endereços de email para enviar a notificação de orçamento para quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="70ae1-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="70ae1-119">-Pessoa de contato</span><span class="sxs-lookup"><span data-stu-id="70ae1-119">-ContactGroup</span></span>
<span data-ttu-id="70ae1-120">Grupos de ações para os quais enviar a notificação de orçamento quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="70ae1-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="70ae1-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="70ae1-121">-ContactRole</span></span>
<span data-ttu-id="70ae1-122">Funções de contato para enviar a notificação de orçamento para quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="70ae1-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="70ae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ae1-123">-DefaultProfile</span></span>
<span data-ttu-id="70ae1-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70ae1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ae1-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="70ae1-125">-EndDate</span></span>
<span data-ttu-id="70ae1-126">Data de término (AAAA-MM-DD em UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="70ae1-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="70ae1-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="70ae1-127">-MeterFilter</span></span>
<span data-ttu-id="70ae1-128">Lista separada por vírgula de medidores para filtrar.</span><span class="sxs-lookup"><span data-stu-id="70ae1-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="70ae1-129">Obrigatório se a categoria for o uso.</span><span class="sxs-lookup"><span data-stu-id="70ae1-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="70ae1-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="70ae1-130">-Name</span></span>
<span data-ttu-id="70ae1-131">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="70ae1-131">Name of a budget.</span></span>

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

### <span data-ttu-id="70ae1-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="70ae1-132">-NotificationEnabled</span></span>
<span data-ttu-id="70ae1-133">A notificação está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="70ae1-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="70ae1-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="70ae1-134">-NotificationKey</span></span>
<span data-ttu-id="70ae1-135">Chave de uma notificação associada a um orçamento, necessária para criar uma notificação com uma chave habilitada para notificação, um limite de notificação, emails de contato, grupos de contatos ou funções de contato.</span><span class="sxs-lookup"><span data-stu-id="70ae1-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="70ae1-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="70ae1-136">-NotificationThreshold</span></span>
<span data-ttu-id="70ae1-137">Valor limite associado a uma notificação.</span><span class="sxs-lookup"><span data-stu-id="70ae1-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="70ae1-138">A notificação é enviada quando o custo ou o uso excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="70ae1-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="70ae1-139">É sempre porcentagem e deve estar entre 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="70ae1-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="70ae1-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="70ae1-140">-ResourceFilter</span></span>
<span data-ttu-id="70ae1-141">Lista separada por vírgula de instâncias de recurso para filtrar.</span><span class="sxs-lookup"><span data-stu-id="70ae1-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="70ae1-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="70ae1-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="70ae1-143">Lista separada por vírgula de grupos de recursos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="70ae1-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="70ae1-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ae1-144">-ResourceGroupName</span></span>
<span data-ttu-id="70ae1-145">Grupo de recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="70ae1-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="70ae1-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="70ae1-146">-StartDate</span></span>
<span data-ttu-id="70ae1-147">Data de início (AAAA-MM-DD em UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="70ae1-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="70ae1-148">Não antes do mês atual para o intervalo de tempo mensal.</span><span class="sxs-lookup"><span data-stu-id="70ae1-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="70ae1-149">Não antes de três meses para o intervalo trimestral de tempo.</span><span class="sxs-lookup"><span data-stu-id="70ae1-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="70ae1-150">Não antes de 12 meses por um intervalo de tempo anual.</span><span class="sxs-lookup"><span data-stu-id="70ae1-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="70ae1-151">Data de início futuro não tem mais de três meses.</span><span class="sxs-lookup"><span data-stu-id="70ae1-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="70ae1-152">-Timegranular</span><span class="sxs-lookup"><span data-stu-id="70ae1-152">-TimeGrain</span></span>
<span data-ttu-id="70ae1-153">O intervalo de tempo do orçamento pode ser mensal, trimestral ou anualmente.</span><span class="sxs-lookup"><span data-stu-id="70ae1-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="70ae1-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70ae1-154">-Confirm</span></span>
<span data-ttu-id="70ae1-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70ae1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ae1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ae1-156">-WhatIf</span></span>
<span data-ttu-id="70ae1-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70ae1-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70ae1-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70ae1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ae1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ae1-159">CommonParameters</span></span>
<span data-ttu-id="70ae1-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ae1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ae1-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ae1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ae1-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70ae1-162">INPUTS</span></span>

### <span data-ttu-id="70ae1-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="70ae1-163">None</span></span>

## <span data-ttu-id="70ae1-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70ae1-164">OUTPUTS</span></span>

### <span data-ttu-id="70ae1-165">Microsoft. Azure. Commands. consumo. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="70ae1-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="70ae1-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70ae1-166">NOTES</span></span>

## <span data-ttu-id="70ae1-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70ae1-167">RELATED LINKS</span></span>
