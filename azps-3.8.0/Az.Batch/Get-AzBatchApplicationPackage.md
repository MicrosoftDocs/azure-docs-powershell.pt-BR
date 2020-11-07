---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944139"
---
# <span data-ttu-id="bd652-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bd652-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="bd652-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd652-102">SYNOPSIS</span></span>
<span data-ttu-id="bd652-103">Obtém informações sobre um pacote de aplicativo em uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="bd652-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="bd652-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd652-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd652-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd652-105">DESCRIPTION</span></span>
<span data-ttu-id="bd652-106">O cmdlet **Get-AzBatchApplicationPackage** Obtém informações sobre um pacote de aplicativo em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd652-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="bd652-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd652-107">EXAMPLES</span></span>

### <span data-ttu-id="bd652-108">Exemplo 1: obter detalhes de um pacote de aplicativo em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="bd652-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="bd652-109">Este comando obtém os detalhes da versão 1,0 do pacote Litware.</span><span class="sxs-lookup"><span data-stu-id="bd652-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="bd652-110">OS</span><span class="sxs-lookup"><span data-stu-id="bd652-110">PARAMETERS</span></span>

### <span data-ttu-id="bd652-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd652-111">-AccountName</span></span>
<span data-ttu-id="bd652-112">Especifica o nome da conta em lotes da qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="bd652-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="bd652-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="bd652-113">-ApplicationName</span></span>
<span data-ttu-id="bd652-114">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd652-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd652-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="bd652-115">-ApplicationVersion</span></span>
<span data-ttu-id="bd652-116">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd652-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd652-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd652-117">-DefaultProfile</span></span>
<span data-ttu-id="bd652-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd652-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd652-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd652-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd652-120">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="bd652-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="bd652-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd652-121">CommonParameters</span></span>
<span data-ttu-id="bd652-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd652-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd652-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd652-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd652-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd652-124">INPUTS</span></span>

### <span data-ttu-id="bd652-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bd652-125">System.String</span></span>

## <span data-ttu-id="bd652-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd652-126">OUTPUTS</span></span>

### <span data-ttu-id="bd652-127">Microsoft.Azure.Commands.Batch. Modelos. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bd652-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="bd652-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd652-128">NOTES</span></span>

## <span data-ttu-id="bd652-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd652-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd652-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bd652-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="bd652-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bd652-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="bd652-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bd652-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="bd652-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bd652-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="bd652-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bd652-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="bd652-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bd652-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


