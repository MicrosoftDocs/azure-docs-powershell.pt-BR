---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 609c7e161b131d80f9b41355f13ced8636a591e8
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441594"
---
# <span data-ttu-id="5d7ee-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5d7ee-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="5d7ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="5d7ee-103">Obtém informações sobre um pacote de aplicativo em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d7ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d7ee-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d7ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d7ee-105">DESCRIPTION</span></span>
<span data-ttu-id="5d7ee-106">O cmdlet **Get-AzureRmBatchApplicationPackage** Obtém informações sobre um pacote de aplicativo em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="5d7ee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d7ee-107">EXAMPLES</span></span>

### <span data-ttu-id="5d7ee-108">Exemplo 1: obter detalhes de um pacote de aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="5d7ee-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="5d7ee-109">Este comando obtém os detalhes da versão 1,0 do pacote Litware.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="5d7ee-110">OS</span><span class="sxs-lookup"><span data-stu-id="5d7ee-110">PARAMETERS</span></span>

### <span data-ttu-id="5d7ee-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d7ee-111">-AccountName</span></span>
<span data-ttu-id="5d7ee-112">Especifica o nome da conta em lotes da qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d7ee-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5d7ee-113">-ApplicationId</span></span>
<span data-ttu-id="5d7ee-114">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d7ee-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="5d7ee-115">-ApplicationVersion</span></span>
<span data-ttu-id="5d7ee-116">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-116">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d7ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d7ee-117">-DefaultProfile</span></span>
<span data-ttu-id="5d7ee-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d7ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d7ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d7ee-120">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-120">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d7ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d7ee-121">CommonParameters</span></span>
<span data-ttu-id="5d7ee-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d7ee-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d7ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d7ee-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d7ee-124">INPUTS</span></span>

### <span data-ttu-id="5d7ee-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5d7ee-125">None</span></span>
<span data-ttu-id="5d7ee-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5d7ee-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d7ee-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d7ee-127">OUTPUTS</span></span>

### <span data-ttu-id="5d7ee-128">Microsoft.Azure.Commands.Batch. Modelos. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5d7ee-128">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="5d7ee-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d7ee-129">NOTES</span></span>

## <span data-ttu-id="5d7ee-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d7ee-130">RELATED LINKS</span></span>

[<span data-ttu-id="5d7ee-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5d7ee-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="5d7ee-132">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5d7ee-132">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="5d7ee-133">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5d7ee-133">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="5d7ee-134">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5d7ee-134">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="5d7ee-135">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="5d7ee-135">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="5d7ee-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="5d7ee-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


