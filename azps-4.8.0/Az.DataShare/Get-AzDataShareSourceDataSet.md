---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955618"
---
# <span data-ttu-id="b2915-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="b2915-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="b2915-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2915-102">SYNOPSIS</span></span>
<span data-ttu-id="b2915-103">Obtém informações sobre conjuntos de dados de origem na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b2915-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="b2915-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2915-104">SYNTAX</span></span>

### <span data-ttu-id="b2915-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2915-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2915-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2915-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2915-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2915-107">DESCRIPTION</span></span>
<span data-ttu-id="b2915-108">O cmdlet **Get-AzDataShareSourceDataSet** fornece informações sobre os conjuntos de dados de origem na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b2915-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="b2915-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2915-109">EXAMPLES</span></span>

### <span data-ttu-id="b2915-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2915-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="b2915-111">Obtém conjuntos de fontes disponíveis no compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="b2915-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="b2915-112">OS</span><span class="sxs-lookup"><span data-stu-id="b2915-112">PARAMETERS</span></span>

### <span data-ttu-id="b2915-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2915-113">-AccountName</span></span>
<span data-ttu-id="b2915-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b2915-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b2915-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2915-115">-DefaultProfile</span></span>
<span data-ttu-id="b2915-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2915-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2915-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2915-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2915-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="b2915-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b2915-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b2915-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="b2915-120">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b2915-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b2915-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="b2915-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="b2915-122">ID do recurso de assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="b2915-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="b2915-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2915-123">CommonParameters</span></span>
<span data-ttu-id="b2915-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2915-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2915-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2915-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2915-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2915-126">INPUTS</span></span>

### <span data-ttu-id="b2915-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b2915-127">System.String</span></span>

## <span data-ttu-id="b2915-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2915-128">OUTPUTS</span></span>

### <span data-ttu-id="b2915-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="b2915-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="b2915-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2915-130">NOTES</span></span>

## <span data-ttu-id="b2915-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2915-131">RELATED LINKS</span></span>
