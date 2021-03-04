---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: a25efdd89e99e52115ade8354d7e96f8ee7972ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890434"
---
# <span data-ttu-id="a3662-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="a3662-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="a3662-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3662-102">SYNOPSIS</span></span>
<span data-ttu-id="a3662-103">Obtém informações sobre mapeamentos de conjuntos de dados na assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="a3662-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="a3662-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a3662-104">SYNTAX</span></span>

### <span data-ttu-id="a3662-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3662-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3662-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3662-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3662-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a3662-107">DESCRIPTION</span></span>
<span data-ttu-id="a3662-108">O cmdlet **Get-AzDataShareDataSetMapping** obtém informações sobre um mapeamento de conjuntos de dados específico se o nome for especificado.</span><span class="sxs-lookup"><span data-stu-id="a3662-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="a3662-109">Caso contrário, ele obtém informações sobre todos os mapeamentos de conjuntos de dados em uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a3662-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="a3662-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3662-110">EXAMPLES</span></span>

### <span data-ttu-id="a3662-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3662-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="a3662-112">Este comando exibe informações sobre todos os mapeamentos de conjuntos de dados na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="a3662-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="a3662-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a3662-113">PARAMETERS</span></span>

### <span data-ttu-id="a3662-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3662-114">-AccountName</span></span>
<span data-ttu-id="a3662-115">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="a3662-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3662-116">-DefaultProfile</span></span>
<span data-ttu-id="a3662-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3662-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a3662-118">-Name</span></span>
<span data-ttu-id="a3662-119">Nome do mapeamento do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="a3662-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3662-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3662-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="a3662-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3662-122">-ResourceId</span></span>
<span data-ttu-id="a3662-123">A id de recurso do mapeamento do conjunto de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="a3662-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3662-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="a3662-125">Nome da assinatura do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3662-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="a3662-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3662-126">CommonParameters</span></span>
<span data-ttu-id="a3662-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3662-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3662-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3662-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3662-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3662-129">INPUTS</span></span>

### <span data-ttu-id="a3662-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a3662-130">System.String</span></span>

## <span data-ttu-id="a3662-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a3662-131">OUTPUTS</span></span>

### <span data-ttu-id="a3662-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="a3662-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="a3662-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="a3662-133">NOTES</span></span>

## <span data-ttu-id="a3662-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3662-134">RELATED LINKS</span></span>
