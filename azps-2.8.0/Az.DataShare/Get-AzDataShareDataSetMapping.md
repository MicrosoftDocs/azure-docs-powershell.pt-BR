---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: d19825fea43e8fc029e960a513d1c2ad306a8406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596742"
---
# <span data-ttu-id="12d8f-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="12d8f-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="12d8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="12d8f-103">Obtém informações sobre mapeamentos de DataSet na assinatura do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="12d8f-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="12d8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12d8f-104">SYNTAX</span></span>

### <span data-ttu-id="12d8f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="12d8f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d8f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d8f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12d8f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="12d8f-108">O cmdlet **Get-AzDataShareDataSetMapping** Obtém informações sobre um mapeamento de DataSet específico se o nome for especificado.</span><span class="sxs-lookup"><span data-stu-id="12d8f-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="12d8f-109">Caso contrário, ele obtém informações sobre todos os mapeamentos de DataSet em uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="12d8f-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="12d8f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12d8f-110">EXAMPLES</span></span>

### <span data-ttu-id="12d8f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12d8f-111">Example 1</span></span>
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

 <span data-ttu-id="12d8f-112">Esse comando exibe informações sobre todos os mapeamentos de DataSet na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="12d8f-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="12d8f-113">OS</span><span class="sxs-lookup"><span data-stu-id="12d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="12d8f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12d8f-114">-AccountName</span></span>
<span data-ttu-id="12d8f-115">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="12d8f-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="12d8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d8f-116">-DefaultProfile</span></span>
<span data-ttu-id="12d8f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12d8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d8f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="12d8f-118">-Name</span></span>
<span data-ttu-id="12d8f-119">Nome do mapeamento do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="12d8f-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="12d8f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d8f-120">-ResourceGroupName</span></span>
<span data-ttu-id="12d8f-121">O nome do grupo de recursos da conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="12d8f-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="12d8f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12d8f-122">-ResourceId</span></span>
<span data-ttu-id="12d8f-123">A ID do recurso do mapeamento do conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="12d8f-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="12d8f-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="12d8f-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="12d8f-125">Nome da assinatura do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="12d8f-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="12d8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d8f-126">CommonParameters</span></span>
<span data-ttu-id="12d8f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d8f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d8f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d8f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12d8f-129">INPUTS</span></span>

### <span data-ttu-id="12d8f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12d8f-130">System.String</span></span>

## <span data-ttu-id="12d8f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12d8f-131">OUTPUTS</span></span>

### <span data-ttu-id="12d8f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="12d8f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="12d8f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12d8f-133">NOTES</span></span>

## <span data-ttu-id="12d8f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12d8f-134">RELATED LINKS</span></span>
