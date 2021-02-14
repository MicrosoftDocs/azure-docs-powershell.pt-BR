---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116595"
---
# <span data-ttu-id="db488-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="db488-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="db488-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db488-102">SYNOPSIS</span></span>
<span data-ttu-id="db488-103">Obter faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="db488-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="db488-104">Obter faturas de cobrança de uma conta de cobrança e perfil de cobrança</span><span class="sxs-lookup"><span data-stu-id="db488-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="db488-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db488-105">SYNTAX</span></span>

### <span data-ttu-id="db488-106">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db488-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="db488-107">Últimas</span><span class="sxs-lookup"><span data-stu-id="db488-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="db488-108">Único</span><span class="sxs-lookup"><span data-stu-id="db488-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db488-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="db488-109">DESCRIPTION</span></span>
<span data-ttu-id="db488-110">O **cmdlet Get-AzBillingInvoice** obtém faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="db488-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="db488-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db488-111">EXAMPLES</span></span>

### <span data-ttu-id="db488-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db488-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="db488-113">Obter a fatura mais recente da assinatura.</span><span class="sxs-lookup"><span data-stu-id="db488-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="db488-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db488-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="db488-115">Obter a fatura da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="db488-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="db488-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db488-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="db488-117">Obter todas as faturas disponíveis da assinatura em ordem cronológica inversa, começando com a fatura mais recente sem baixar a URL.</span><span class="sxs-lookup"><span data-stu-id="db488-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="db488-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="db488-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="db488-119">Receba as 10 faturas mais recentes da assinatura e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="db488-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="db488-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="db488-121">Obter a fatura específica por nome e incluir a URL do download no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="db488-122">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="db488-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="db488-123">Obter faturas pelo nome da conta de cobrança e incluir a URL de download de cada fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="db488-124">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="db488-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="db488-125">Receba uma fatura específica pelo nome da fatura e pelo nome da conta de cobrança e inclua a URL de download de cada fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="db488-126">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="db488-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="db488-127">Receba a fatura mais recente pelo nome da conta de cobrança e inclua a URL de download da fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="db488-128">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="db488-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="db488-129">Receba as 10 faturas mais recentes da conta de cobrança específica e do perfil de cobrança específico e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="db488-130">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="db488-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="db488-131">Receba a fatura mais recente por meio do nome da conta de cobrança e do nome do perfil de cobrança e inclua a URL de download da fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="db488-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="db488-132">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="db488-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="db488-133">Obter faturas com o nome da conta de cobrança e o nome do perfil de cobrança para um período de cobrança especificado pela data de início e data do períodoEnd.</span><span class="sxs-lookup"><span data-stu-id="db488-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="db488-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db488-134">PARAMETERS</span></span>

### <span data-ttu-id="db488-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db488-135">-DefaultProfile</span></span>
<span data-ttu-id="db488-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="db488-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db488-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="db488-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="db488-138">Gere a URL de download das faturas.</span><span class="sxs-lookup"><span data-stu-id="db488-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="db488-139">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="db488-139">-Latest</span></span>
<span data-ttu-id="db488-140">Obter a fatura mais recente.</span><span class="sxs-lookup"><span data-stu-id="db488-140">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="db488-141">-MaxCount</span></span>
<span data-ttu-id="db488-142">Determina o número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="db488-142">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="db488-143">-Name</span></span>
<span data-ttu-id="db488-144">Nome de uma fatura específica para obter ou a mais recente, se não especificada.</span><span class="sxs-lookup"><span data-stu-id="db488-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="db488-145">-BillingAccountName</span></span>
<span data-ttu-id="db488-146">Nome de uma conta de cobrança específica para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="db488-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="db488-147">-BillingProfileName</span></span>
<span data-ttu-id="db488-148">Nome de um perfil de cobrança específico para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="db488-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="db488-149">-PeriodStartDate</span></span>
<span data-ttu-id="db488-150">Data de início da fatura.</span><span class="sxs-lookup"><span data-stu-id="db488-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db488-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="db488-151">-PeriodEndDate</span></span>
<span data-ttu-id="db488-152">Data de término da fatura.</span><span class="sxs-lookup"><span data-stu-id="db488-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="db488-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db488-153">CommonParameters</span></span>
<span data-ttu-id="db488-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db488-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db488-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db488-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db488-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="db488-156">INPUTS</span></span>

### <span data-ttu-id="db488-157">Nenhum</span><span class="sxs-lookup"><span data-stu-id="db488-157">None</span></span>

## <span data-ttu-id="db488-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="db488-158">OUTPUTS</span></span>

### <span data-ttu-id="db488-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="db488-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="db488-160">Notas</span><span class="sxs-lookup"><span data-stu-id="db488-160">NOTES</span></span>

## <span data-ttu-id="db488-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db488-161">RELATED LINKS</span></span>
