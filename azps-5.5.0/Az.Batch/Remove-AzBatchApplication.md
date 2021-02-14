---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115527"
---
# <span data-ttu-id="55a58-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a58-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="55a58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55a58-102">SYNOPSIS</span></span>
<span data-ttu-id="55a58-103">Exclui um aplicativo de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="55a58-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="55a58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55a58-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55a58-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="55a58-105">DESCRIPTION</span></span>
<span data-ttu-id="55a58-106">O **cmdlet Remove-AzBatchApplication** exclui um aplicativo de uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="55a58-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="55a58-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55a58-107">EXAMPLES</span></span>

### <span data-ttu-id="55a58-108">Exemplo 1: Excluir um aplicativo de uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="55a58-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="55a58-109">Esse comando exclui o aplicativo Litware da conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="55a58-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="55a58-110">O comando falhará se o aplicativo contiver pacotes.</span><span class="sxs-lookup"><span data-stu-id="55a58-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="55a58-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55a58-111">PARAMETERS</span></span>

### <span data-ttu-id="55a58-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="55a58-112">-AccountName</span></span>
<span data-ttu-id="55a58-113">Especifica o nome da conta Em lotes da qual este cmdlet remove um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55a58-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="55a58-114">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="55a58-114">-ApplicationName</span></span>
<span data-ttu-id="55a58-115">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="55a58-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="55a58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a58-116">-DefaultProfile</span></span>
<span data-ttu-id="55a58-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="55a58-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55a58-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a58-118">-ResourceGroupName</span></span>
<span data-ttu-id="55a58-119">Especifica o nome do grupo de recursos que contém a conta Lote.</span><span class="sxs-lookup"><span data-stu-id="55a58-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="55a58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a58-120">CommonParameters</span></span>
<span data-ttu-id="55a58-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a58-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55a58-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a58-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="55a58-123">INPUTS</span></span>

### <span data-ttu-id="55a58-124">System.String</span><span class="sxs-lookup"><span data-stu-id="55a58-124">System.String</span></span>

## <span data-ttu-id="55a58-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="55a58-125">OUTPUTS</span></span>

### <span data-ttu-id="55a58-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="55a58-126">System.Void</span></span>

## <span data-ttu-id="55a58-127">Notas</span><span class="sxs-lookup"><span data-stu-id="55a58-127">NOTES</span></span>

## <span data-ttu-id="55a58-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55a58-128">RELATED LINKS</span></span>

[<span data-ttu-id="55a58-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a58-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="55a58-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a58-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="55a58-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a58-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="55a58-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a58-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="55a58-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a58-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="55a58-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a58-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


