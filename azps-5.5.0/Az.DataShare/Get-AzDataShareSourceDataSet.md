---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127024"
---
# <span data-ttu-id="255c9-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="255c9-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="255c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="255c9-102">SYNOPSIS</span></span>
<span data-ttu-id="255c9-103">Obtém informações sobre conjuntos de dados de origem na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="255c9-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="255c9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="255c9-104">SYNTAX</span></span>

### <span data-ttu-id="255c9-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="255c9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="255c9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="255c9-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="255c9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="255c9-107">DESCRIPTION</span></span>
<span data-ttu-id="255c9-108">O cmdlet **Get-AzDataShareSourceDataSet** fornece informações sobre os conjuntos de dados de origem na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="255c9-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="255c9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="255c9-109">EXAMPLES</span></span>

### <span data-ttu-id="255c9-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="255c9-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="255c9-111">Obtém conjuntos de dados disponíveis no compartilhamento de origem</span><span class="sxs-lookup"><span data-stu-id="255c9-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="255c9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="255c9-112">PARAMETERS</span></span>

### <span data-ttu-id="255c9-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="255c9-113">-AccountName</span></span>
<span data-ttu-id="255c9-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="255c9-114">Azure data share account name</span></span>

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

### <span data-ttu-id="255c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255c9-115">-DefaultProfile</span></span>
<span data-ttu-id="255c9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="255c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="255c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="255c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="255c9-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="255c9-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="255c9-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="255c9-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="255c9-120">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="255c9-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="255c9-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="255c9-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="255c9-122">ID do recurso de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="255c9-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="255c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255c9-123">CommonParameters</span></span>
<span data-ttu-id="255c9-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255c9-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="255c9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255c9-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="255c9-126">INPUTS</span></span>

### <span data-ttu-id="255c9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="255c9-127">System.String</span></span>

## <span data-ttu-id="255c9-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="255c9-128">OUTPUTS</span></span>

### <span data-ttu-id="255c9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="255c9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="255c9-130">Notas</span><span class="sxs-lookup"><span data-stu-id="255c9-130">NOTES</span></span>

## <span data-ttu-id="255c9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="255c9-131">RELATED LINKS</span></span>
