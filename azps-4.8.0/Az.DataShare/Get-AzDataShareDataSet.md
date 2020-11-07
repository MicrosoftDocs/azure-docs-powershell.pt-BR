---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948342"
---
# <span data-ttu-id="950d0-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="950d0-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="950d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="950d0-102">SYNOPSIS</span></span>
<span data-ttu-id="950d0-103">Obtém informações sobre conjuntos de dados no compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="950d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="950d0-104">SYNTAX</span></span>

### <span data-ttu-id="950d0-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="950d0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="950d0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="950d0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="950d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="950d0-107">DESCRIPTION</span></span>
<span data-ttu-id="950d0-108">O cmdlet **Get-AzDataShareDataSet** Obtém informações sobre conjuntos de dados adicionados em um compartilhamento em uma conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="950d0-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="950d0-109">Se você especificar o nome do conjunto de dados, esse cmdlet obterá informações sobre o conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="950d0-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="950d0-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados em um compartilhamento. Configur</span><span class="sxs-lookup"><span data-stu-id="950d0-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="950d0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="950d0-111">EXAMPLES</span></span>

### <span data-ttu-id="950d0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="950d0-112">Example 1</span></span>
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

<span data-ttu-id="950d0-113">Esse comando exibe informações sobre o conjunto de dados AdsDataSet no share AdsShare no Azure data share WikiAdsAccount e em grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="950d0-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="950d0-114">OS</span><span class="sxs-lookup"><span data-stu-id="950d0-114">PARAMETERS</span></span>

### <span data-ttu-id="950d0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="950d0-115">-AccountName</span></span>
<span data-ttu-id="950d0-116">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="950d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950d0-117">-DefaultProfile</span></span>
<span data-ttu-id="950d0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="950d0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="950d0-119">-Name</span></span>
<span data-ttu-id="950d0-120">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-120">Azure data set name.</span></span>

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

### <span data-ttu-id="950d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="950d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="950d0-122">O nome do grupo de recursos da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="950d0-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="950d0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="950d0-123">-ResourceId</span></span>
<span data-ttu-id="950d0-124">A ID do recurso do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="950d0-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="950d0-125">-ShareName</span></span>
<span data-ttu-id="950d0-126">Nome de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="950d0-126">Azure data share name.</span></span>

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

### <span data-ttu-id="950d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950d0-127">CommonParameters</span></span>
<span data-ttu-id="950d0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="950d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950d0-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="950d0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950d0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="950d0-130">INPUTS</span></span>

### <span data-ttu-id="950d0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="950d0-131">System.String</span></span>

## <span data-ttu-id="950d0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="950d0-132">OUTPUTS</span></span>

### <span data-ttu-id="950d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="950d0-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="950d0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="950d0-134">NOTES</span></span>

## <span data-ttu-id="950d0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="950d0-135">RELATED LINKS</span></span>
