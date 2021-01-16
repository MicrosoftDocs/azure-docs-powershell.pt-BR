---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259829"
---
# <span data-ttu-id="1cc00-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cc00-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="1cc00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cc00-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc00-103">Obtém informações sobre o aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="1cc00-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="1cc00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cc00-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cc00-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cc00-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc00-106">O cmdlet **Get-AzBatchApplication** Obtém informações sobre um aplicativo em uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc00-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="1cc00-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cc00-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc00-108">Exemplo 1: exibir os aplicativos em uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="1cc00-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="1cc00-109">Esse comando exibe todos os aplicativos na conta do ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="1cc00-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="1cc00-110">OS</span><span class="sxs-lookup"><span data-stu-id="1cc00-110">PARAMETERS</span></span>

### <span data-ttu-id="1cc00-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1cc00-111">-AccountName</span></span>
<span data-ttu-id="1cc00-112">Especifica o nome da conta em lotes que contém o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cc00-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="1cc00-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1cc00-113">-ApplicationName</span></span>
<span data-ttu-id="1cc00-114">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1cc00-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc00-115">-DefaultProfile</span></span>
<span data-ttu-id="1cc00-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc00-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cc00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc00-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cc00-118">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="1cc00-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="1cc00-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc00-119">CommonParameters</span></span>
<span data-ttu-id="1cc00-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc00-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc00-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cc00-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc00-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cc00-122">INPUTS</span></span>

### <span data-ttu-id="1cc00-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1cc00-123">System.String</span></span>

## <span data-ttu-id="1cc00-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cc00-124">OUTPUTS</span></span>

### <span data-ttu-id="1cc00-125">Microsoft.Azure.Commands.Batch. Modelos. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1cc00-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="1cc00-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cc00-126">NOTES</span></span>

## <span data-ttu-id="1cc00-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cc00-127">RELATED LINKS</span></span>

[<span data-ttu-id="1cc00-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cc00-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="1cc00-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cc00-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="1cc00-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cc00-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="1cc00-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cc00-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="1cc00-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="1cc00-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="1cc00-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="1cc00-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


