---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 302129506c516cd0f2864210d5323b83fb54e0df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602960"
---
# <span data-ttu-id="8e2be-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e2be-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8e2be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e2be-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2be-103">Aguarda um trabalho ser concluído.</span><span class="sxs-lookup"><span data-stu-id="8e2be-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e2be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e2be-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e2be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e2be-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2be-106">O cmdlet **Wait-AzureRmDataLakeAnalyticsJob** aguarda a conclusão de um trabalho do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e2be-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="8e2be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e2be-107">EXAMPLES</span></span>

### <span data-ttu-id="8e2be-108">Exemplo 1: Aguarde a conclusão do trabalho</span><span class="sxs-lookup"><span data-stu-id="8e2be-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="8e2be-109">O comando a seguir aguarda o trabalho com a ID especificada ser concluída.</span><span class="sxs-lookup"><span data-stu-id="8e2be-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="8e2be-110">OS</span><span class="sxs-lookup"><span data-stu-id="8e2be-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2be-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="8e2be-111">-Account</span></span>
<span data-ttu-id="8e2be-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8e2be-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8e2be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2be-113">-DefaultProfile</span></span>
<span data-ttu-id="8e2be-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8e2be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e2be-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="8e2be-115">-JobId</span></span>
<span data-ttu-id="8e2be-116">Especifica a ID do trabalho a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="8e2be-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2be-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e2be-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="8e2be-118">Especifica o número de segundos a aguardar antes de sair da operação de espera.</span><span class="sxs-lookup"><span data-stu-id="8e2be-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2be-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e2be-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="8e2be-120">Especifique o número de segundos que decorrem entre cada verificação do estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e2be-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2be-121">CommonParameters</span></span>
<span data-ttu-id="8e2be-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2be-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2be-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2be-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e2be-124">INPUTS</span></span>

### <span data-ttu-id="8e2be-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8e2be-125">System.String</span></span>

### <span data-ttu-id="8e2be-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8e2be-126">System.Guid</span></span>

### <span data-ttu-id="8e2be-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8e2be-127">System.Int32</span></span>

## <span data-ttu-id="8e2be-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e2be-128">OUTPUTS</span></span>

### <span data-ttu-id="8e2be-129">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="8e2be-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="8e2be-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e2be-130">NOTES</span></span>

## <span data-ttu-id="8e2be-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e2be-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e2be-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e2be-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="8e2be-133">Parar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e2be-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="8e2be-134">Enviar-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8e2be-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


