---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2707100452f9b64c093b4ae52c724e09f6cfe6e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429826"
---
# <span data-ttu-id="4018a-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4018a-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="4018a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4018a-102">SYNOPSIS</span></span>
<span data-ttu-id="4018a-103">Remove uma fonte de dados de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4018a-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4018a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4018a-104">SYNTAX</span></span>

### <span data-ttu-id="4018a-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4018a-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4018a-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4018a-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4018a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4018a-107">DESCRIPTION</span></span>
<span data-ttu-id="4018a-108">O cmdlet **Remove-AzureRmDataLakeAnalyticsDataSource** remove uma fonte de dados de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4018a-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4018a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4018a-109">EXAMPLES</span></span>

### <span data-ttu-id="4018a-110">Exemplo 1: remover uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="4018a-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="4018a-111">Esse comando Remove a fonte de dados chamada AzureStorage01 da conta chamada ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="4018a-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="4018a-112">OS</span><span class="sxs-lookup"><span data-stu-id="4018a-112">PARAMETERS</span></span>

### <span data-ttu-id="4018a-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="4018a-113">-Account</span></span>
<span data-ttu-id="4018a-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4018a-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="4018a-115">-Blob</span></span>
<span data-ttu-id="4018a-116">Especifica o nome da conta de armazenamento do AzureBlob a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4018a-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4018a-117">-DataLakeStore</span></span>
<span data-ttu-id="4018a-118">Especifica o nome da conta da AzureData Lake Store a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4018a-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4018a-119">-DefaultProfile</span></span>
<span data-ttu-id="4018a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4018a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4018a-121">-Force</span></span>
<span data-ttu-id="4018a-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4018a-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4018a-123">-PassThru</span></span>
<span data-ttu-id="4018a-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4018a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4018a-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4018a-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4018a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4018a-127">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4018a-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4018a-128">-Confirm</span></span>
<span data-ttu-id="4018a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4018a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4018a-130">-WhatIf</span></span>
<span data-ttu-id="4018a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4018a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4018a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4018a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4018a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4018a-133">CommonParameters</span></span>
<span data-ttu-id="4018a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4018a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4018a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4018a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4018a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4018a-136">INPUTS</span></span>

### <span data-ttu-id="4018a-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4018a-137">None</span></span>
<span data-ttu-id="4018a-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4018a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4018a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4018a-139">OUTPUTS</span></span>

### <span data-ttu-id="4018a-140">bool</span><span class="sxs-lookup"><span data-stu-id="4018a-140">bool</span></span>
<span data-ttu-id="4018a-141">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="4018a-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="4018a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4018a-142">NOTES</span></span>

## <span data-ttu-id="4018a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4018a-143">RELATED LINKS</span></span>

[<span data-ttu-id="4018a-144">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4018a-144">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="4018a-145">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="4018a-145">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


