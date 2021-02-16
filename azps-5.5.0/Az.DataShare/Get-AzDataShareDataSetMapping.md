---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116416"
---
# <span data-ttu-id="83c58-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="83c58-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="83c58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83c58-102">SYNOPSIS</span></span>
<span data-ttu-id="83c58-103">Obtém informações sobre mapeamentos de conjuntos de dados na assinatura de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="83c58-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="83c58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83c58-104">SYNTAX</span></span>

### <span data-ttu-id="83c58-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="83c58-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83c58-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c58-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83c58-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="83c58-107">DESCRIPTION</span></span>
<span data-ttu-id="83c58-108">O cmdlet **Get-AzDataShareDataSetMapping** obtém informações sobre um mapeamento de conjuntos de dados específico se o nome for especificado.</span><span class="sxs-lookup"><span data-stu-id="83c58-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="83c58-109">Caso contrário, ele obtém informações sobre todos os mapeamentos de conjuntos de dados em uma assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="83c58-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="83c58-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83c58-110">EXAMPLES</span></span>

### <span data-ttu-id="83c58-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83c58-111">Example 1</span></span>
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

 <span data-ttu-id="83c58-112">Esse comando exibe informações sobre todos os mapeamentos de conjuntos de dados na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="83c58-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="83c58-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83c58-113">PARAMETERS</span></span>

### <span data-ttu-id="83c58-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="83c58-114">-AccountName</span></span>
<span data-ttu-id="83c58-115">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="83c58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c58-116">-DefaultProfile</span></span>
<span data-ttu-id="83c58-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83c58-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="83c58-118">-Name</span></span>
<span data-ttu-id="83c58-119">Nome de mapeamento de conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="83c58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c58-120">-ResourceGroupName</span></span>
<span data-ttu-id="83c58-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="83c58-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83c58-122">-ResourceId</span></span>
<span data-ttu-id="83c58-123">A ID do recurso do mapeamento de conjunto de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="83c58-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="83c58-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="83c58-125">Nome da assinatura do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="83c58-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="83c58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c58-126">CommonParameters</span></span>
<span data-ttu-id="83c58-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c58-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83c58-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c58-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="83c58-129">INPUTS</span></span>

### <span data-ttu-id="83c58-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83c58-130">System.String</span></span>

## <span data-ttu-id="83c58-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="83c58-131">OUTPUTS</span></span>

### <span data-ttu-id="83c58-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="83c58-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="83c58-133">Notas</span><span class="sxs-lookup"><span data-stu-id="83c58-133">NOTES</span></span>

## <span data-ttu-id="83c58-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83c58-134">RELATED LINKS</span></span>
