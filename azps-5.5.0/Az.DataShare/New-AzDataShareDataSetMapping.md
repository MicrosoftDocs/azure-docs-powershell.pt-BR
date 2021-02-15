---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113860"
---
# <span data-ttu-id="0162b-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="0162b-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="0162b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0162b-102">SYNOPSIS</span></span>
<span data-ttu-id="0162b-103">Cria mapeamento de conjunto de dados para compartilhar assinatura.</span><span class="sxs-lookup"><span data-stu-id="0162b-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="0162b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0162b-104">SYNTAX</span></span>

### <span data-ttu-id="0162b-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0162b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0162b-106">ByBdataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="0162b-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0162b-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="0162b-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0162b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0162b-108">DESCRIPTION</span></span>
<span data-ttu-id="0162b-109">O cmdlet **New-AzDataShareDataSetMapping** cria um mapeamento de conjunto de dados entre os conjuntos de dados de origem e a conta de armazenamento de estouro na assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="0162b-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="0162b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0162b-110">EXAMPLES</span></span>

### <span data-ttu-id="0162b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0162b-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="0162b-112">Esse comando cria um conjunto de dados mapeando AdsDataSetMapping para a conta de armazenamento AdsStorage para compartilhar assinatura AdsShareSubscription na conta de compartilhamento de dados WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="0162b-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="0162b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0162b-113">PARAMETERS</span></span>

### <span data-ttu-id="0162b-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="0162b-114">-AccountName</span></span>
<span data-ttu-id="0162b-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-116">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="0162b-116">-Container</span></span>
<span data-ttu-id="0162b-117">Nome do contêiner da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="0162b-118">-DataSetId</span></span>
<span data-ttu-id="0162b-119">ID do conjunto de dados do consumidor</span><span class="sxs-lookup"><span data-stu-id="0162b-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0162b-120">-DefaultProfile</span></span>
<span data-ttu-id="0162b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0162b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0162b-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0162b-122">-FilePath</span></span>
<span data-ttu-id="0162b-123">Caminho de arquivo de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="0162b-124">-FileSystem</span></span>
<span data-ttu-id="0162b-125">Nome do sistema de arquivos do Azure ADLS gen2</span><span class="sxs-lookup"><span data-stu-id="0162b-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="0162b-126">-FolderPath</span></span>
<span data-ttu-id="0162b-127">Caminho da pasta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="0162b-128">-Name</span></span>
<span data-ttu-id="0162b-129">Nome de mapeamento de conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0162b-130">-ResourceGroupName</span></span>
<span data-ttu-id="0162b-131">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="0162b-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0162b-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="0162b-133">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0162b-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="0162b-135">ResourceId da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0162b-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0162b-136">-Confirm</span></span>
<span data-ttu-id="0162b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0162b-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0162b-138">-WhatIf</span></span>
<span data-ttu-id="0162b-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0162b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0162b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0162b-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0162b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0162b-141">CommonParameters</span></span>
<span data-ttu-id="0162b-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0162b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0162b-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0162b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0162b-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="0162b-144">INPUTS</span></span>

### <span data-ttu-id="0162b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0162b-145">System.String</span></span>

## <span data-ttu-id="0162b-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="0162b-146">OUTPUTS</span></span>

### <span data-ttu-id="0162b-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="0162b-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="0162b-148">Notas</span><span class="sxs-lookup"><span data-stu-id="0162b-148">NOTES</span></span>

## <span data-ttu-id="0162b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0162b-149">RELATED LINKS</span></span>
