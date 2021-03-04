---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 751fa50a6c29c826fe707852efa661b78d1b9c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892185"
---
# <span data-ttu-id="09fca-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="09fca-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="09fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09fca-102">SYNOPSIS</span></span>
<span data-ttu-id="09fca-103">Obtém um Trabalho de Análise do Data Lake recorrências ou recorrências.</span><span class="sxs-lookup"><span data-stu-id="09fca-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="09fca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09fca-104">SYNTAX</span></span>

### <span data-ttu-id="09fca-105">GetAllInAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09fca-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09fca-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="09fca-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09fca-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09fca-107">DESCRIPTION</span></span>
<span data-ttu-id="09fca-108">**Get-AzDataLakeAnalyticsJobRecurrence** obtém uma recorrência especificada do Trabalho de Análise do Azure Data Lake ou uma lista de recorrência.</span><span class="sxs-lookup"><span data-stu-id="09fca-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="09fca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09fca-109">EXAMPLES</span></span>

### <span data-ttu-id="09fca-110">Exemplo 1: Obter uma recorrência especificada</span><span class="sxs-lookup"><span data-stu-id="09fca-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="09fca-111">Este comando obtém a recorrência de trabalho especificada com a id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="09fca-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="09fca-112">Exemplo 2: Obter uma lista de todas as recorrências na conta</span><span class="sxs-lookup"><span data-stu-id="09fca-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="09fca-113">Este comando obtém uma lista de todas as recorrências na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="09fca-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="09fca-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09fca-114">PARAMETERS</span></span>

### <span data-ttu-id="09fca-115">-Account</span><span class="sxs-lookup"><span data-stu-id="09fca-115">-Account</span></span>
<span data-ttu-id="09fca-116">Nome do nome da conta do Data Lake Analytics sob o qual deseja recuperar a recorrência do trabalho.</span><span class="sxs-lookup"><span data-stu-id="09fca-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fca-117">-DefaultProfile</span></span>
<span data-ttu-id="09fca-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="09fca-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09fca-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="09fca-119">-RecurrenceId</span></span>
<span data-ttu-id="09fca-120">ID da recorrência de trabalho específica para retornar informações.</span><span class="sxs-lookup"><span data-stu-id="09fca-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09fca-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="09fca-121">-SubmittedAfter</span></span>
<span data-ttu-id="09fca-122">Um filtro opcional que retorna as recorrências de trabalho enviadas somente após o horário especificado.</span><span class="sxs-lookup"><span data-stu-id="09fca-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fca-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="09fca-123">-SubmittedBefore</span></span>
<span data-ttu-id="09fca-124">Um filtro opcional que retorna as recorrências de trabalho enviadas somente antes do horário especificado.</span><span class="sxs-lookup"><span data-stu-id="09fca-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fca-125">CommonParameters</span></span>
<span data-ttu-id="09fca-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fca-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fca-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fca-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09fca-128">INPUTS</span></span>

### <span data-ttu-id="09fca-129">System.String</span><span class="sxs-lookup"><span data-stu-id="09fca-129">System.String</span></span>

### <span data-ttu-id="09fca-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="09fca-130">System.Guid</span></span>

### <span data-ttu-id="09fca-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09fca-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="09fca-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09fca-132">OUTPUTS</span></span>

### <span data-ttu-id="09fca-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="09fca-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="09fca-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="09fca-134">NOTES</span></span>

## <span data-ttu-id="09fca-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09fca-135">RELATED LINKS</span></span>
