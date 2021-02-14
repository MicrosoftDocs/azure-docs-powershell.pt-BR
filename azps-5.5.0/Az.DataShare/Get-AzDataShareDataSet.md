---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110981"
---
# <span data-ttu-id="cc426-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="cc426-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="cc426-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc426-102">SYNOPSIS</span></span>
<span data-ttu-id="cc426-103">Obtém informações sobre Conjuntos de Dados no compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="cc426-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc426-104">SYNTAX</span></span>

### <span data-ttu-id="cc426-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc426-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc426-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc426-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc426-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc426-107">DESCRIPTION</span></span>
<span data-ttu-id="cc426-108">O **cmdlet Get-AzDataShareDataSet** obtém informações sobre conjuntos de dados adicionados em um compartilhamento em uma conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="cc426-109">Se você especificar o nome do conjunto de dados, esse cmdlet obterá informações sobre o conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="cc426-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="cc426-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados em um compartilhamento. Eu</span><span class="sxs-lookup"><span data-stu-id="cc426-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="cc426-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cc426-111">EXAMPLES</span></span>

### <span data-ttu-id="cc426-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc426-112">Example 1</span></span>
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

<span data-ttu-id="cc426-113">Esse comando exibe informações sobre o conjunto de dados AdsDataSet no share AdsShare na conta de compartilhamento de dados wikiAdsAccount do Azure e ADS do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc426-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="cc426-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc426-114">PARAMETERS</span></span>

### <span data-ttu-id="cc426-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="cc426-115">-AccountName</span></span>
<span data-ttu-id="cc426-116">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="cc426-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc426-117">-DefaultProfile</span></span>
<span data-ttu-id="cc426-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc426-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc426-119">-Name</span></span>
<span data-ttu-id="cc426-120">Nome do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-120">Azure data set name.</span></span>

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

### <span data-ttu-id="cc426-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc426-121">-ResourceGroupName</span></span>
<span data-ttu-id="cc426-122">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="cc426-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc426-123">-ResourceId</span></span>
<span data-ttu-id="cc426-124">A ID do recurso do conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="cc426-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cc426-125">-ShareName</span></span>
<span data-ttu-id="cc426-126">Nome do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc426-126">Azure data share name.</span></span>

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

### <span data-ttu-id="cc426-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc426-127">CommonParameters</span></span>
<span data-ttu-id="cc426-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc426-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc426-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc426-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc426-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="cc426-130">INPUTS</span></span>

### <span data-ttu-id="cc426-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cc426-131">System.String</span></span>

## <span data-ttu-id="cc426-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="cc426-132">OUTPUTS</span></span>

### <span data-ttu-id="cc426-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="cc426-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="cc426-134">Notas</span><span class="sxs-lookup"><span data-stu-id="cc426-134">NOTES</span></span>

## <span data-ttu-id="cc426-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc426-135">RELATED LINKS</span></span>
