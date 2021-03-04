---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: d0bf60bbfd13474270391afd6f01bc9ec8130b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890435"
---
# <span data-ttu-id="63a52-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="63a52-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="63a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a52-102">SYNOPSIS</span></span>
<span data-ttu-id="63a52-103">Obtém informações sobre conjuntos de dados no compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="63a52-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63a52-104">SYNTAX</span></span>

### <span data-ttu-id="63a52-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63a52-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63a52-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a52-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a52-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63a52-107">DESCRIPTION</span></span>
<span data-ttu-id="63a52-108">O cmdlet **Get-AzDataShareDataSet** obtém informações sobre conjuntos de dados adicionados em um compartilhamento em uma conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="63a52-109">Se você especificar o nome do conjunto de dados, esse cmdlet obterá informações sobre o conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="63a52-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="63a52-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados em um compartilhamento. I</span><span class="sxs-lookup"><span data-stu-id="63a52-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="63a52-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63a52-111">EXAMPLES</span></span>

### <span data-ttu-id="63a52-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63a52-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="63a52-113">Este comando exibe informações sobre o conjunto de dados AdsDataSet no compartilhamento AdsShare na conta de compartilhamento de dados do Azure WikiAdsAccount e ADS do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63a52-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="63a52-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63a52-114">PARAMETERS</span></span>

### <span data-ttu-id="63a52-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63a52-115">-AccountName</span></span>
<span data-ttu-id="63a52-116">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="63a52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a52-117">-DefaultProfile</span></span>
<span data-ttu-id="63a52-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a52-119">-Name</span><span class="sxs-lookup"><span data-stu-id="63a52-119">-Name</span></span>
<span data-ttu-id="63a52-120">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a52-121">-ResourceGroupName</span></span>
<span data-ttu-id="63a52-122">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="63a52-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63a52-123">-ResourceId</span></span>
<span data-ttu-id="63a52-124">A id de recurso do conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="63a52-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="63a52-125">-ShareName</span></span>
<span data-ttu-id="63a52-126">Nome do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="63a52-126">Azure data share name.</span></span>

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

### <span data-ttu-id="63a52-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a52-127">CommonParameters</span></span>
<span data-ttu-id="63a52-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a52-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a52-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63a52-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a52-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63a52-130">INPUTS</span></span>

### <span data-ttu-id="63a52-131">System.String</span><span class="sxs-lookup"><span data-stu-id="63a52-131">System.String</span></span>

## <span data-ttu-id="63a52-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63a52-132">OUTPUTS</span></span>

### <span data-ttu-id="63a52-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="63a52-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="63a52-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="63a52-134">NOTES</span></span>

## <span data-ttu-id="63a52-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63a52-135">RELATED LINKS</span></span>
