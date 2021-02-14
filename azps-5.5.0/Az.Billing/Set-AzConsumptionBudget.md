---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115965"
---
# <span data-ttu-id="260df-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="260df-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="260df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="260df-102">SYNOPSIS</span></span>
<span data-ttu-id="260df-103">Atualize um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="260df-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="260df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="260df-104">SYNTAX</span></span>

### <span data-ttu-id="260df-105">Assinatura (Padrão)</span><span class="sxs-lookup"><span data-stu-id="260df-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260df-106">Notificação</span><span class="sxs-lookup"><span data-stu-id="260df-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260df-107">Tubulação</span><span class="sxs-lookup"><span data-stu-id="260df-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="260df-108">Piping e Notification</span><span class="sxs-lookup"><span data-stu-id="260df-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="260df-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="260df-109">DESCRIPTION</span></span>
<span data-ttu-id="260df-110">O Set-AzConsumptionBudget cmdlet atualiza um orçamento em uma assinatura ou em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="260df-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="260df-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="260df-111">EXAMPLES</span></span>

### <span data-ttu-id="260df-112">Exemplo 1: Atualizar um orçamento em um novo valor com um nome de orçamento no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="260df-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="260df-113">Exemplo 2: Atualizar um orçamento com uma notificação quando o custo ou o uso atingir um limite de 90% do valor no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="260df-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="260df-114">Exemplo 3: Atualizar um orçamento em um novo valor com um nome de orçamento no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="260df-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="260df-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="260df-115">PARAMETERS</span></span>

### <span data-ttu-id="260df-116">-Valor</span><span class="sxs-lookup"><span data-stu-id="260df-116">-Amount</span></span>
<span data-ttu-id="260df-117">Valor de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-118">-Categoria</span><span class="sxs-lookup"><span data-stu-id="260df-118">-Category</span></span>
<span data-ttu-id="260df-119">A categoria do orçamento pode ser custo ou uso.</span><span class="sxs-lookup"><span data-stu-id="260df-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="260df-120">-ContactEmail</span></span>
<span data-ttu-id="260df-121">Endereços de email para enviar a notificação de orçamento quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="260df-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="260df-122">-ContactGroup</span></span>
<span data-ttu-id="260df-123">Grupos de ações para enviar a notificação de orçamento quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="260df-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="260df-124">-ContactRole</span></span>
<span data-ttu-id="260df-125">Funções de contato para enviar a notificação de orçamento para quando o limite for excedido.</span><span class="sxs-lookup"><span data-stu-id="260df-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260df-126">-DefaultProfile</span></span>
<span data-ttu-id="260df-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="260df-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="260df-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="260df-128">-EndDate</span></span>
<span data-ttu-id="260df-129">Data de término (AAAA-DD-MM no UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="260df-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="260df-130">-InputObject</span></span>
<span data-ttu-id="260df-131">Objeto de orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="260df-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="260df-132">-MeterFilter</span></span>
<span data-ttu-id="260df-133">Lista de metros separados por vírgulas para filtrar.</span><span class="sxs-lookup"><span data-stu-id="260df-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="260df-134">Obrigatório se categoria for o uso.</span><span class="sxs-lookup"><span data-stu-id="260df-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="260df-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="260df-135">-Name</span></span>
<span data-ttu-id="260df-136">Nome de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="260df-137">-NotificationEnabled</span></span>
<span data-ttu-id="260df-138">A notificação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="260df-138">The notification is enabled.</span></span>
<span data-ttu-id="260df-139">Se não especificado, a notificação será desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="260df-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="260df-140">-NotificationKey</span></span>
<span data-ttu-id="260df-141">Chave de uma notificação associada a um orçamento, necessária para criar uma notificação com opção habilitada para notificação, limite de notificação, emails de contato, grupos de contatos ou funções de contato.</span><span class="sxs-lookup"><span data-stu-id="260df-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="260df-142">-NotificationThreshold</span></span>
<span data-ttu-id="260df-143">Valor limite associado a uma notificação.</span><span class="sxs-lookup"><span data-stu-id="260df-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="260df-144">A notificação é enviada quando o custo ou o uso excedeu o limite.</span><span class="sxs-lookup"><span data-stu-id="260df-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="260df-145">Ela sempre é porcentagem e deve estar entre 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="260df-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="260df-146">-ResourceFilter</span></span>
<span data-ttu-id="260df-147">Lista separada por vírgulas de instâncias de recurso para filtrar.</span><span class="sxs-lookup"><span data-stu-id="260df-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="260df-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="260df-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="260df-149">Lista separada por vírgulas de grupos de recursos para filtrar.</span><span class="sxs-lookup"><span data-stu-id="260df-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="260df-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260df-150">-ResourceGroupName</span></span>
<span data-ttu-id="260df-151">Grupo de Recursos de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-152">-Data Inicial</span><span class="sxs-lookup"><span data-stu-id="260df-152">-StartDate</span></span>
<span data-ttu-id="260df-153">Data de início (AAAA-DD-MM no UTC) do período de tempo de um orçamento.</span><span class="sxs-lookup"><span data-stu-id="260df-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="260df-154">Não antes do mês atual para o tempo mensal.</span><span class="sxs-lookup"><span data-stu-id="260df-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="260df-155">Não antes de três meses para o tempo trimestral.</span><span class="sxs-lookup"><span data-stu-id="260df-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="260df-156">Não antes de doze meses para a hora anual.</span><span class="sxs-lookup"><span data-stu-id="260df-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="260df-157">Data de início futura, não mais do que três meses.</span><span class="sxs-lookup"><span data-stu-id="260df-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="260df-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="260df-158">-TimeGrain</span></span>
<span data-ttu-id="260df-159">O tempo do orçamento pode ser mensal, trimestral ou anual.</span><span class="sxs-lookup"><span data-stu-id="260df-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260df-160">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="260df-160">-Confirm</span></span>
<span data-ttu-id="260df-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="260df-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="260df-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260df-162">-WhatIf</span></span>
<span data-ttu-id="260df-163">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="260df-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260df-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="260df-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="260df-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260df-165">CommonParameters</span></span>
<span data-ttu-id="260df-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260df-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260df-167">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260df-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260df-168">Entradas</span><span class="sxs-lookup"><span data-stu-id="260df-168">INPUTS</span></span>

### <span data-ttu-id="260df-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="260df-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="260df-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="260df-170">OUTPUTS</span></span>

### <span data-ttu-id="260df-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="260df-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="260df-172">Notas</span><span class="sxs-lookup"><span data-stu-id="260df-172">NOTES</span></span>

## <span data-ttu-id="260df-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="260df-173">RELATED LINKS</span></span>
