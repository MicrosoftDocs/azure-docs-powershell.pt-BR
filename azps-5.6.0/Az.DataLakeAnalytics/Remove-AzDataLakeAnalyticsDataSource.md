---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: d5ea5e1131768c747a959af97ed541daefd4587b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888707"
---
# <span data-ttu-id="f2520-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2520-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="f2520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2520-102">SYNOPSIS</span></span>
<span data-ttu-id="f2520-103">Remove uma fonte de dados de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2520-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2520-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2520-104">SYNTAX</span></span>

### <span data-ttu-id="f2520-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2520-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2520-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2520-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2520-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2520-107">DESCRIPTION</span></span>
<span data-ttu-id="f2520-108">O cmdlet **Remove-AzDataLakeAnalyticsDataSource** remove uma fonte de dados de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2520-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2520-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2520-109">EXAMPLES</span></span>

### <span data-ttu-id="f2520-110">Exemplo 1: Remover uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="f2520-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="f2520-111">Este comando remove a fonte de dados chamada AzureStorage01 da conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="f2520-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="f2520-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2520-112">PARAMETERS</span></span>

### <span data-ttu-id="f2520-113">-Account</span><span class="sxs-lookup"><span data-stu-id="f2520-113">-Account</span></span>
<span data-ttu-id="f2520-114">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2520-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="f2520-115">-Blob</span></span>
<span data-ttu-id="f2520-116">Especifica o nome da conta de Armazenamento do AzureBlob a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2520-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f2520-117">-DataLakeStore</span></span>
<span data-ttu-id="f2520-118">Especifica o nome da conta do AzureData Lake Store a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2520-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2520-119">-DefaultProfile</span></span>
<span data-ttu-id="f2520-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f2520-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2520-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f2520-121">-Force</span></span>
<span data-ttu-id="f2520-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f2520-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2520-123">-PassThru</span></span>
<span data-ttu-id="f2520-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f2520-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2520-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f2520-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2520-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2520-127">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2520-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2520-128">-Confirm</span></span>
<span data-ttu-id="f2520-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2520-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2520-130">-WhatIf</span></span>
<span data-ttu-id="f2520-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2520-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2520-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2520-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2520-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2520-133">CommonParameters</span></span>
<span data-ttu-id="f2520-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2520-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2520-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2520-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2520-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2520-136">INPUTS</span></span>

### <span data-ttu-id="f2520-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f2520-137">System.String</span></span>

## <span data-ttu-id="f2520-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2520-138">OUTPUTS</span></span>

### <span data-ttu-id="f2520-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2520-139">System.Boolean</span></span>

## <span data-ttu-id="f2520-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2520-140">NOTES</span></span>

## <span data-ttu-id="f2520-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2520-141">RELATED LINKS</span></span>

[<span data-ttu-id="f2520-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2520-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="f2520-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2520-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


