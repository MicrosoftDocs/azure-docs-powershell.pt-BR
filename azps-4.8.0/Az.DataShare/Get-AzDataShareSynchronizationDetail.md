---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947828"
---
# <span data-ttu-id="0d80b-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="0d80b-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="0d80b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d80b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d80b-103">Obtém informações sobre os detalhes da sincronização de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0d80b-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="0d80b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d80b-104">SYNTAX</span></span>

### <span data-ttu-id="0d80b-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d80b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d80b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d80b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d80b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d80b-107">DESCRIPTION</span></span>
<span data-ttu-id="0d80b-108">O cmdlet **Get-AzDataShareSynchronizationDetail** fornece detalhes da sincronização iniciada para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0d80b-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="0d80b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d80b-109">EXAMPLES</span></span>

### <span data-ttu-id="0d80b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d80b-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="0d80b-111">Esse comando fornece informações sobre os detalhes da sincronização de todos os conjuntos de dados correspondentes à ID de sincronização fornecida.</span><span class="sxs-lookup"><span data-stu-id="0d80b-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="0d80b-112">OS</span><span class="sxs-lookup"><span data-stu-id="0d80b-112">PARAMETERS</span></span>

### <span data-ttu-id="0d80b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0d80b-113">-AccountName</span></span>
<span data-ttu-id="0d80b-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0d80b-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d80b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d80b-115">-DefaultProfile</span></span>
<span data-ttu-id="0d80b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d80b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d80b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d80b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d80b-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="0d80b-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d80b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d80b-119">-ResourceId</span></span>
<span data-ttu-id="0d80b-120">ID do recurso de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0d80b-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d80b-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0d80b-121">-ShareName</span></span>
<span data-ttu-id="0d80b-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0d80b-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d80b-123">-Synchronizationid</span><span class="sxs-lookup"><span data-stu-id="0d80b-123">-SynchronizationId</span></span>
<span data-ttu-id="0d80b-124">ID de sincronização da sincronização de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="0d80b-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="0d80b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d80b-125">CommonParameters</span></span>
<span data-ttu-id="0d80b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d80b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d80b-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d80b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d80b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d80b-128">INPUTS</span></span>

### <span data-ttu-id="0d80b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0d80b-129">System.String</span></span>

## <span data-ttu-id="0d80b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d80b-130">OUTPUTS</span></span>

### <span data-ttu-id="0d80b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="0d80b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="0d80b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d80b-132">NOTES</span></span>

## <span data-ttu-id="0d80b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d80b-133">RELATED LINKS</span></span>
