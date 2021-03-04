---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: b32c0d7db6a55a560733380c66e971c614fabc71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887912"
---
# <span data-ttu-id="741bc-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="741bc-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="741bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741bc-102">SYNOPSIS</span></span>
<span data-ttu-id="741bc-103">Obtém informações sobre o aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="741bc-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="741bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="741bc-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="741bc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="741bc-105">DESCRIPTION</span></span>
<span data-ttu-id="741bc-106">O cmdlet **Get-AzBatchApplication** obtém informações sobre um aplicativo em uma conta do Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="741bc-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="741bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="741bc-107">EXAMPLES</span></span>

### <span data-ttu-id="741bc-108">Exemplo 1: Exibir os aplicativos em uma conta batch</span><span class="sxs-lookup"><span data-stu-id="741bc-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="741bc-109">Este comando exibe todos os aplicativos na conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="741bc-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="741bc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="741bc-110">PARAMETERS</span></span>

### <span data-ttu-id="741bc-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="741bc-111">-AccountName</span></span>
<span data-ttu-id="741bc-112">Especifica o nome da conta Batch que contém o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="741bc-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="741bc-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="741bc-113">-ApplicationName</span></span>
<span data-ttu-id="741bc-114">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="741bc-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="741bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741bc-115">-DefaultProfile</span></span>
<span data-ttu-id="741bc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="741bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="741bc-118">Especifica o nome do grupo de recursos que contém a conta Batch.</span><span class="sxs-lookup"><span data-stu-id="741bc-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="741bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741bc-119">CommonParameters</span></span>
<span data-ttu-id="741bc-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741bc-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="741bc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741bc-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="741bc-122">INPUTS</span></span>

### <span data-ttu-id="741bc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="741bc-123">System.String</span></span>

## <span data-ttu-id="741bc-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="741bc-124">OUTPUTS</span></span>

### <span data-ttu-id="741bc-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="741bc-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="741bc-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="741bc-126">NOTES</span></span>

## <span data-ttu-id="741bc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="741bc-127">RELATED LINKS</span></span>

[<span data-ttu-id="741bc-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="741bc-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="741bc-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="741bc-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="741bc-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="741bc-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="741bc-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="741bc-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="741bc-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="741bc-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="741bc-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="741bc-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


