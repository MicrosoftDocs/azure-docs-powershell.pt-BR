---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886355"
---
# <span data-ttu-id="6c370-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="6c370-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="6c370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c370-102">SYNOPSIS</span></span>
<span data-ttu-id="6c370-103">Obter faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c370-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="6c370-104">Obter faturas de cobrança de uma conta de cobrança e perfil de cobrança</span><span class="sxs-lookup"><span data-stu-id="6c370-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="6c370-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6c370-105">SYNTAX</span></span>

### <span data-ttu-id="6c370-106">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6c370-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="6c370-107">Mais recente</span><span class="sxs-lookup"><span data-stu-id="6c370-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="6c370-108">Single</span><span class="sxs-lookup"><span data-stu-id="6c370-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c370-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6c370-109">DESCRIPTION</span></span>
<span data-ttu-id="6c370-110">O cmdlet **Get-AzBillingInvoice** obtém faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c370-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="6c370-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c370-111">EXAMPLES</span></span>

### <span data-ttu-id="6c370-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6c370-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="6c370-113">Obter a fatura mais recente da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6c370-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="6c370-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6c370-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="6c370-115">Obter a fatura da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="6c370-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="6c370-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6c370-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="6c370-117">Obter todas as faturas disponíveis da assinatura em ordem cronológica inversa começando com a fatura mais recente sem baixar Url.</span><span class="sxs-lookup"><span data-stu-id="6c370-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="6c370-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="6c370-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="6c370-119">Obter as 10 faturas mais recentes da assinatura e incluir a Url de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="6c370-120">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="6c370-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="6c370-121">Obter a fatura específica pelo nome e incluir url de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="6c370-122">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="6c370-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="6c370-123">Obter faturas pelo nome da conta de cobrança e incluir url de download para cada fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="6c370-124">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="6c370-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="6c370-125">Obter fatura específica pelo nome da fatura e o nome da conta de cobrança e incluir url de download para cada fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="6c370-126">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="6c370-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="6c370-127">Obter a fatura mais recente pelo nome da conta de cobrança e incluir url de download para fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="6c370-128">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="6c370-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="6c370-129">Obter as 10 faturas mais recentes da conta de cobrança específica e o perfil de cobrança específico e incluir a Url de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="6c370-130">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="6c370-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="6c370-131">Obter a fatura mais recente cobrando o nome da conta e o nome do perfil de cobrança e inclua a URL de download da fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="6c370-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="6c370-132">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="6c370-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="6c370-133">Obter faturas pelo nome da conta de cobrança e o nome do perfil de cobrança para um período de cobrança especificado pela data perioStart e data periodEnd.</span><span class="sxs-lookup"><span data-stu-id="6c370-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="6c370-134">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6c370-134">PARAMETERS</span></span>

### <span data-ttu-id="6c370-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c370-135">-DefaultProfile</span></span>
<span data-ttu-id="6c370-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6c370-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c370-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="6c370-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="6c370-138">Gere a URL de download das faturas.</span><span class="sxs-lookup"><span data-stu-id="6c370-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="6c370-139">-Latest</span><span class="sxs-lookup"><span data-stu-id="6c370-139">-Latest</span></span>
<span data-ttu-id="6c370-140">Obter a fatura mais recente.</span><span class="sxs-lookup"><span data-stu-id="6c370-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="6c370-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6c370-141">-MaxCount</span></span>
<span data-ttu-id="6c370-142">Determina o número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="6c370-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="6c370-143">-Name</span><span class="sxs-lookup"><span data-stu-id="6c370-143">-Name</span></span>
<span data-ttu-id="6c370-144">Nome de uma fatura específica para obter ou a mais recente, se não especificada.</span><span class="sxs-lookup"><span data-stu-id="6c370-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="6c370-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="6c370-145">-BillingAccountName</span></span>
<span data-ttu-id="6c370-146">Nome de uma conta de cobrança específica para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="6c370-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="6c370-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="6c370-147">-BillingProfileName</span></span>
<span data-ttu-id="6c370-148">Nome de um perfil de cobrança específico para obter faturas.</span><span class="sxs-lookup"><span data-stu-id="6c370-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="6c370-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="6c370-149">-PeriodStartDate</span></span>
<span data-ttu-id="6c370-150">Data de início da fatura.</span><span class="sxs-lookup"><span data-stu-id="6c370-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="6c370-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="6c370-151">-PeriodEndDate</span></span>
<span data-ttu-id="6c370-152">Data de término da fatura.</span><span class="sxs-lookup"><span data-stu-id="6c370-152">End date for invoice.</span></span>

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



### <span data-ttu-id="6c370-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c370-153">CommonParameters</span></span>
<span data-ttu-id="6c370-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c370-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c370-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c370-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c370-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c370-156">INPUTS</span></span>

### <span data-ttu-id="6c370-157">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6c370-157">None</span></span>

## <span data-ttu-id="6c370-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6c370-158">OUTPUTS</span></span>

### <span data-ttu-id="6c370-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="6c370-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="6c370-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="6c370-160">NOTES</span></span>

## <span data-ttu-id="6c370-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c370-161">RELATED LINKS</span></span>
