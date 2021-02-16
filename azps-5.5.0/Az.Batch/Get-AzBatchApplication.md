---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: efdcab51a8dfa6d886a317fa1707b65861cf2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117971"
---
# <span data-ttu-id="e3c19-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e3c19-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="e3c19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3c19-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c19-103">Obtém informações sobre o aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="e3c19-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="e3c19-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3c19-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3c19-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3c19-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c19-106">O cmdlet **Get-AzBatchApplication** obtém informações sobre um aplicativo em uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="e3c19-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="e3c19-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3c19-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c19-108">Exemplo 1: Exibir os aplicativos em uma conta em lote</span><span class="sxs-lookup"><span data-stu-id="e3c19-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationName AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="e3c19-109">Esse comando exibe todos os aplicativos da conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="e3c19-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="e3c19-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3c19-110">PARAMETERS</span></span>

### <span data-ttu-id="e3c19-111">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="e3c19-111">-AccountName</span></span>
<span data-ttu-id="e3c19-112">Especifica o nome da conta em lotes que contém o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3c19-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="e3c19-113">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3c19-113">-ApplicationName</span></span>
<span data-ttu-id="e3c19-114">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3c19-114">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="e3c19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c19-115">-DefaultProfile</span></span>
<span data-ttu-id="e3c19-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e3c19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c19-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3c19-118">Especifica o nome do grupo de recursos que contém a conta Lote.</span><span class="sxs-lookup"><span data-stu-id="e3c19-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="e3c19-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c19-119">CommonParameters</span></span>
<span data-ttu-id="e3c19-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c19-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c19-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3c19-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c19-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3c19-122">INPUTS</span></span>

### <span data-ttu-id="e3c19-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c19-123">System.String</span></span>

## <span data-ttu-id="e3c19-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3c19-124">OUTPUTS</span></span>

### <span data-ttu-id="e3c19-125">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="e3c19-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="e3c19-126">Notas</span><span class="sxs-lookup"><span data-stu-id="e3c19-126">NOTES</span></span>

## <span data-ttu-id="e3c19-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3c19-127">RELATED LINKS</span></span>

[<span data-ttu-id="e3c19-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e3c19-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="e3c19-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e3c19-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="e3c19-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e3c19-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="e3c19-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e3c19-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="e3c19-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="e3c19-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="e3c19-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="e3c19-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


