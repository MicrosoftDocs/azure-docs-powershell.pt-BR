---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: 34d2921526f54e20697a11cf17708fef50e49fc2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428956"
---
# <span data-ttu-id="f1887-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="f1887-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="f1887-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1887-102">SYNOPSIS</span></span>
<span data-ttu-id="f1887-103">Obtém uma recorrência ou recorrências de trabalho do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f1887-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1887-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1887-104">SYNTAX</span></span>

### <span data-ttu-id="f1887-105">GetAllInAccount (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1887-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1887-106">GetBySpecificJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="f1887-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1887-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1887-107">DESCRIPTION</span></span>
<span data-ttu-id="f1887-108">**Get-AzureRmDataLakeAnalyticsJobRecurrence** Obtém uma recorrência de trabalho do Azure data Lake Analytics especificada ou uma lista de recorrência.</span><span class="sxs-lookup"><span data-stu-id="f1887-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="f1887-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1887-109">EXAMPLES</span></span>

### <span data-ttu-id="f1887-110">Exemplo 1: obter uma recorrência especificada</span><span class="sxs-lookup"><span data-stu-id="f1887-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="f1887-111">Este comando obtém a recorrência do trabalho especificado com a ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="f1887-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="f1887-112">Exemplo 2: obter uma lista de todas as recorrências na conta</span><span class="sxs-lookup"><span data-stu-id="f1887-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="f1887-113">Esse comando obtém uma lista de todas as recorrências na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="f1887-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="f1887-114">OS</span><span class="sxs-lookup"><span data-stu-id="f1887-114">PARAMETERS</span></span>

### <span data-ttu-id="f1887-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="f1887-115">-Account</span></span>
<span data-ttu-id="f1887-116">Nome do nome da conta do data Lake Analytics sob a qual deseja recuperar a recorrência do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f1887-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1887-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1887-117">-DefaultProfile</span></span>
<span data-ttu-id="f1887-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f1887-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1887-119">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="f1887-119">-RecurrenceId</span></span>
<span data-ttu-id="f1887-120">ID da recorrência de trabalho específica para a qual as informações são retornadas.</span><span class="sxs-lookup"><span data-stu-id="f1887-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1887-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="f1887-121">-SubmittedAfter</span></span>
<span data-ttu-id="f1887-122">Um filtro opcional que retorna as recorrências de trabalho somente enviadas após a hora especificada.</span><span class="sxs-lookup"><span data-stu-id="f1887-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1887-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="f1887-123">-SubmittedBefore</span></span>
<span data-ttu-id="f1887-124">Um filtro opcional que retorna as recorrências de trabalho somente enviadas antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="f1887-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1887-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1887-125">CommonParameters</span></span>
<span data-ttu-id="f1887-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1887-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1887-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1887-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1887-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1887-128">INPUTS</span></span>

### <span data-ttu-id="f1887-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f1887-129">System.String</span></span>
<span data-ttu-id="f1887-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f1887-130">System.Guid</span></span>

## <span data-ttu-id="f1887-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1887-131">OUTPUTS</span></span>

### <span data-ttu-id="f1887-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="f1887-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="f1887-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1887-133">NOTES</span></span>

## <span data-ttu-id="f1887-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1887-134">RELATED LINKS</span></span>

