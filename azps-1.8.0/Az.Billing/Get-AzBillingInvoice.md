---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 8c5e107de50d5e1df1f0c9da7305dbe801857410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601451"
---
# <span data-ttu-id="2ec2a-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="2ec2a-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="2ec2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ec2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec2a-103">Obter faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="2ec2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ec2a-104">SYNTAX</span></span>

### <span data-ttu-id="2ec2a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ec2a-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec2a-106">Novidades</span><span class="sxs-lookup"><span data-stu-id="2ec2a-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ec2a-107">Apenas</span><span class="sxs-lookup"><span data-stu-id="2ec2a-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ec2a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ec2a-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec2a-109">O cmdlet **Get-AzBillingInvoice** recebe faturas de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="2ec2a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ec2a-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec2a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ec2a-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="2ec2a-112">Obtenha a última fatura da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="2ec2a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ec2a-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="2ec2a-114">Obter a fatura da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="2ec2a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2ec2a-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="2ec2a-116">Obtenha todas as faturas disponíveis da assinatura em ordem cronológica inversa, começando com a fatura mais recente sem baixar a URL.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="2ec2a-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="2ec2a-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="2ec2a-118">Obtenha 10 faturas mais recentes da assinatura e inclua a URL de download no resultado.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="2ec2a-119">OS</span><span class="sxs-lookup"><span data-stu-id="2ec2a-119">PARAMETERS</span></span>

### <span data-ttu-id="2ec2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec2a-120">-DefaultProfile</span></span>
<span data-ttu-id="2ec2a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2ec2a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ec2a-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="2ec2a-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="2ec2a-123">Gerar a URL de download das faturas.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec2a-124">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="2ec2a-124">-Latest</span></span>
<span data-ttu-id="2ec2a-125">Obtenha a última fatura.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="2ec2a-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2ec2a-126">-MaxCount</span></span>
<span data-ttu-id="2ec2a-127">Determina o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="2ec2a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ec2a-128">-Name</span></span>
<span data-ttu-id="2ec2a-129">Nome de uma fatura específica a ser obtida ou a mais recente se não for especificada.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="2ec2a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec2a-130">CommonParameters</span></span>
<span data-ttu-id="2ec2a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec2a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec2a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec2a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec2a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ec2a-133">INPUTS</span></span>

### <span data-ttu-id="2ec2a-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ec2a-134">None</span></span>

## <span data-ttu-id="2ec2a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ec2a-135">OUTPUTS</span></span>

### <span data-ttu-id="2ec2a-136">Microsoft. Azure. Commands. billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="2ec2a-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="2ec2a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ec2a-137">NOTES</span></span>

## <span data-ttu-id="2ec2a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ec2a-138">RELATED LINKS</span></span>
