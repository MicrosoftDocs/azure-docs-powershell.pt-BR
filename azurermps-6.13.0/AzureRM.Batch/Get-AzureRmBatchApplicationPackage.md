---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 5e0be2a9c9ba56fecee9e7c1e7ae37a3e39be110
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429592"
---
# <span data-ttu-id="d268e-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d268e-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="d268e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d268e-102">SYNOPSIS</span></span>
<span data-ttu-id="d268e-103">Obtém informações sobre um pacote de aplicativo em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d268e-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d268e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d268e-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d268e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d268e-105">DESCRIPTION</span></span>
<span data-ttu-id="d268e-106">O cmdlet **Get-AzureRmBatchApplicationPackage** Obtém informações sobre um pacote de aplicativo em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="d268e-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="d268e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d268e-107">EXAMPLES</span></span>

### <span data-ttu-id="d268e-108">Exemplo 1: obter detalhes de um pacote de aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="d268e-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="d268e-109">Este comando obtém os detalhes da versão 1,0 do pacote Litware.</span><span class="sxs-lookup"><span data-stu-id="d268e-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="d268e-110">OS</span><span class="sxs-lookup"><span data-stu-id="d268e-110">PARAMETERS</span></span>

### <span data-ttu-id="d268e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d268e-111">-AccountName</span></span>
<span data-ttu-id="d268e-112">Especifica o nome da conta em lotes da qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="d268e-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d268e-113">-ApplicationId</span></span>
<span data-ttu-id="d268e-114">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d268e-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="d268e-115">-ApplicationVersion</span></span>
<span data-ttu-id="d268e-116">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d268e-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d268e-117">-DefaultProfile</span></span>
<span data-ttu-id="d268e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d268e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d268e-119">-ResourceGroupName</span></span>
<span data-ttu-id="d268e-120">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d268e-120">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d268e-121">CommonParameters</span></span>
<span data-ttu-id="d268e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d268e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d268e-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d268e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d268e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d268e-124">INPUTS</span></span>

### <span data-ttu-id="d268e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d268e-125">System.String</span></span>

## <span data-ttu-id="d268e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d268e-126">OUTPUTS</span></span>

### <span data-ttu-id="d268e-127">Microsoft.Azure.Commands.Batch. Modelos. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d268e-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="d268e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d268e-128">NOTES</span></span>

## <span data-ttu-id="d268e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d268e-129">RELATED LINKS</span></span>

[<span data-ttu-id="d268e-130">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d268e-130">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d268e-131">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d268e-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d268e-132">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d268e-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d268e-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d268e-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d268e-134">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d268e-134">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d268e-135">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d268e-135">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


