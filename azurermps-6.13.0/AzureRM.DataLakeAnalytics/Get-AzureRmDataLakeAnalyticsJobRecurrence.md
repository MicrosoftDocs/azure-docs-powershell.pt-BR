---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d0430b283f122b5da41392a04fc9827bc03e3082
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609810"
---
# <span data-ttu-id="d84f2-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d84f2-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="d84f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d84f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d84f2-103">Obtém uma recorrência ou recorrências de trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d84f2-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d84f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d84f2-104">SYNTAX</span></span>

### <span data-ttu-id="d84f2-105">GetAllInAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="d84f2-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d84f2-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="d84f2-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d84f2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d84f2-107">DESCRIPTION</span></span>
<span data-ttu-id="d84f2-108">**Get-AzureRmDataLakeAnalyticsJobRecurrence** Obtém uma recorrência de trabalho do Azure data Lake Analytics especificada ou uma lista de recorrência.</span><span class="sxs-lookup"><span data-stu-id="d84f2-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="d84f2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d84f2-109">EXAMPLES</span></span>

### <span data-ttu-id="d84f2-110">Exemplo 1: obter uma recorrência especificada</span><span class="sxs-lookup"><span data-stu-id="d84f2-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="d84f2-111">Este comando obtém a recorrência do trabalho especificado com a ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="d84f2-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="d84f2-112">Exemplo 2: obter uma lista de todas as recorrências na conta</span><span class="sxs-lookup"><span data-stu-id="d84f2-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="d84f2-113">Esse comando obtém uma lista de todas as recorrências na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="d84f2-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="d84f2-114">OS</span><span class="sxs-lookup"><span data-stu-id="d84f2-114">PARAMETERS</span></span>

### <span data-ttu-id="d84f2-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="d84f2-115">-Account</span></span>
<span data-ttu-id="d84f2-116">Nome do nome da conta do data Lake Analytics sob a qual deseja recuperar a recorrência do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d84f2-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="d84f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84f2-117">-DefaultProfile</span></span>
<span data-ttu-id="d84f2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d84f2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d84f2-119">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="d84f2-119">-RecurrenceId</span></span>
<span data-ttu-id="d84f2-120">ID da recorrência de trabalho específica para a qual as informações são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d84f2-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="d84f2-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d84f2-121">-SubmittedAfter</span></span>
<span data-ttu-id="d84f2-122">Um filtro opcional que retorna as recorrências de trabalho somente enviadas após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="d84f2-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="d84f2-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d84f2-123">-SubmittedBefore</span></span>
<span data-ttu-id="d84f2-124">Um filtro opcional que retorna as recorrências de trabalho somente enviadas antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d84f2-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="d84f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84f2-125">CommonParameters</span></span>
<span data-ttu-id="d84f2-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84f2-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84f2-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d84f2-128">INPUTS</span></span>

### <span data-ttu-id="d84f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d84f2-129">System.String</span></span>

### <span data-ttu-id="d84f2-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d84f2-130">System.Guid</span></span>

### <span data-ttu-id="d84f2-131">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d84f2-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d84f2-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d84f2-132">OUTPUTS</span></span>

### <span data-ttu-id="d84f2-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="d84f2-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="d84f2-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d84f2-134">NOTES</span></span>

## <span data-ttu-id="d84f2-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d84f2-135">RELATED LINKS</span></span>
