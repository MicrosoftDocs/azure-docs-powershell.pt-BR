---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956011"
---
# <span data-ttu-id="c6a0a-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c6a0a-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="c6a0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a0a-103">Adiciona um aplicativo à conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="c6a0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6a0a-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a0a-106">O cmdlet **New-AzBatchApplication** adiciona um aplicativo à conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="c6a0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6a0a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a0a-108">Exemplo 1: adicionar um aplicativo vazio a uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="c6a0a-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="c6a0a-109">Esse comando cria o aplicativo Litware na conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="c6a0a-110">O aplicativo inicialmente não contém pacotes.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="c6a0a-111">OS</span><span class="sxs-lookup"><span data-stu-id="c6a0a-111">PARAMETERS</span></span>

### <span data-ttu-id="c6a0a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6a0a-112">-AccountName</span></span>
<span data-ttu-id="c6a0a-113">Especifica o nome da conta em lotes para a qual esse cmdlet adiciona um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="c6a0a-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="c6a0a-114">-AllowUpdates</span></span>
<span data-ttu-id="c6a0a-115">Especifica se os pacotes dentro do aplicativo podem ser substituídos usando a mesma cadeia de caracteres de versão.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a0a-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c6a0a-116">-ApplicationName</span></span>
<span data-ttu-id="c6a0a-117">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="c6a0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a0a-118">-DefaultProfile</span></span>
<span data-ttu-id="c6a0a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a0a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6a0a-120">-DisplayName</span></span>
<span data-ttu-id="c6a0a-121">Especifica o nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="c6a0a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a0a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c6a0a-123">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c6a0a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a0a-124">CommonParameters</span></span>
<span data-ttu-id="c6a0a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a0a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a0a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6a0a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a0a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6a0a-127">INPUTS</span></span>

### <span data-ttu-id="c6a0a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c6a0a-128">System.String</span></span>

### <span data-ttu-id="c6a0a-129">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c6a0a-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c6a0a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6a0a-130">OUTPUTS</span></span>

### <span data-ttu-id="c6a0a-131">Microsoft.Azure.Commands.Batch. Modelos. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c6a0a-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="c6a0a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6a0a-132">NOTES</span></span>

## <span data-ttu-id="c6a0a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6a0a-133">RELATED LINKS</span></span>

[<span data-ttu-id="c6a0a-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c6a0a-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="c6a0a-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c6a0a-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="c6a0a-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c6a0a-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="c6a0a-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c6a0a-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="c6a0a-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c6a0a-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="c6a0a-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c6a0a-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


