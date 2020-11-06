---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610127"
---
# <span data-ttu-id="d2815-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2815-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="d2815-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2815-102">SYNOPSIS</span></span>
<span data-ttu-id="d2815-103">Adiciona um aplicativo à conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="d2815-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2815-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2815-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2815-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2815-105">DESCRIPTION</span></span>
<span data-ttu-id="d2815-106">O cmdlet **New-AzureRmBatchApplication** adiciona um aplicativo à conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="d2815-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d2815-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2815-107">EXAMPLES</span></span>

### <span data-ttu-id="d2815-108">Exemplo 1: adicionar um aplicativo vazio a uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="d2815-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="d2815-109">Esse comando cria o aplicativo Litware na conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="d2815-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="d2815-110">O aplicativo inicialmente não contém pacotes.</span><span class="sxs-lookup"><span data-stu-id="d2815-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="d2815-111">OS</span><span class="sxs-lookup"><span data-stu-id="d2815-111">PARAMETERS</span></span>

### <span data-ttu-id="d2815-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2815-112">-AccountName</span></span>
<span data-ttu-id="d2815-113">Especifica o nome da conta em lotes para a qual esse cmdlet adiciona um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2815-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="d2815-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="d2815-114">-AllowUpdates</span></span>
<span data-ttu-id="d2815-115">Especifica se os pacotes dentro do aplicativo podem ser substituídos usando a mesma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="d2815-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2815-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d2815-116">-ApplicationId</span></span>
<span data-ttu-id="d2815-117">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2815-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d2815-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2815-118">-DefaultProfile</span></span>
<span data-ttu-id="d2815-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2815-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2815-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d2815-120">-DisplayName</span></span>
<span data-ttu-id="d2815-121">Especifica o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2815-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="d2815-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2815-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2815-123">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="d2815-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d2815-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2815-124">CommonParameters</span></span>
<span data-ttu-id="d2815-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2815-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2815-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2815-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2815-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2815-127">INPUTS</span></span>

### <span data-ttu-id="d2815-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2815-128">None</span></span>
<span data-ttu-id="d2815-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d2815-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d2815-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2815-130">OUTPUTS</span></span>

### <span data-ttu-id="d2815-131">Microsoft.Azure.Commands.Batch. Modelos. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d2815-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="d2815-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2815-132">NOTES</span></span>

## <span data-ttu-id="d2815-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2815-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2815-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2815-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d2815-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2815-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2815-136">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2815-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2815-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2815-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d2815-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2815-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2815-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2815-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


