---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: b8169b2f05b4272c92989768e672b30aee105f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439966"
---
# <span data-ttu-id="cae20-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cae20-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="cae20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cae20-102">SYNOPSIS</span></span>
<span data-ttu-id="cae20-103">Obtém informações sobre o aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="cae20-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cae20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cae20-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cae20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cae20-105">DESCRIPTION</span></span>
<span data-ttu-id="cae20-106">O cmdlet **Get-AzureRmBatchApplication** Obtém informações sobre um aplicativo em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="cae20-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="cae20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cae20-107">EXAMPLES</span></span>

### <span data-ttu-id="cae20-108">Exemplo 1: exibir os aplicativos em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="cae20-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="cae20-109">Esse comando exibe todos os aplicativos na conta do ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="cae20-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="cae20-110">OS</span><span class="sxs-lookup"><span data-stu-id="cae20-110">PARAMETERS</span></span>

### <span data-ttu-id="cae20-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cae20-111">-AccountName</span></span>
<span data-ttu-id="cae20-112">Especifica o nome da conta em lotes que contém o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cae20-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="cae20-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cae20-113">-ApplicationId</span></span>
<span data-ttu-id="cae20-114">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cae20-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae20-115">-ResourceGroupName</span></span>
<span data-ttu-id="cae20-116">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="cae20-116">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="cae20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae20-117">-DefaultProfile</span></span>
<span data-ttu-id="cae20-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cae20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae20-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae20-119">CommonParameters</span></span>
<span data-ttu-id="cae20-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae20-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae20-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae20-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae20-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cae20-122">INPUTS</span></span>

## <span data-ttu-id="cae20-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cae20-123">OUTPUTS</span></span>

### <span data-ttu-id="cae20-124">Microsoft.Azure.Commands.Batch. Modelos. PSApplication</span><span class="sxs-lookup"><span data-stu-id="cae20-124">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="cae20-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cae20-125">NOTES</span></span>

## <span data-ttu-id="cae20-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cae20-126">RELATED LINKS</span></span>

[<span data-ttu-id="cae20-127">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cae20-127">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="cae20-128">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cae20-128">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="cae20-129">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cae20-129">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="cae20-130">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cae20-130">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="cae20-131">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="cae20-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="cae20-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="cae20-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


