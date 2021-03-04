---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: ebe28df5c69ce966a9d05d2e34cd9e66693d7f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890657"
---
# <span data-ttu-id="92bdc-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92bdc-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="92bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="92bdc-103">Exclui um aplicativo de uma conta Batch.</span><span class="sxs-lookup"><span data-stu-id="92bdc-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="92bdc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92bdc-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92bdc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="92bdc-106">O cmdlet **Remove-AzBatchApplication** exclui um aplicativo de uma conta batch do Azure.</span><span class="sxs-lookup"><span data-stu-id="92bdc-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="92bdc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92bdc-107">EXAMPLES</span></span>

### <span data-ttu-id="92bdc-108">Exemplo 1: Excluir um aplicativo de uma conta batch</span><span class="sxs-lookup"><span data-stu-id="92bdc-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="92bdc-109">Este comando exclui o aplicativo Litware da conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="92bdc-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="92bdc-110">O comando falhará se o aplicativo contiver pacotes.</span><span class="sxs-lookup"><span data-stu-id="92bdc-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="92bdc-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92bdc-111">PARAMETERS</span></span>

### <span data-ttu-id="92bdc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92bdc-112">-AccountName</span></span>
<span data-ttu-id="92bdc-113">Especifica o nome da conta Batch da qual esse cmdlet remove um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92bdc-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="92bdc-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="92bdc-114">-ApplicationName</span></span>
<span data-ttu-id="92bdc-115">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92bdc-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="92bdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bdc-116">-DefaultProfile</span></span>
<span data-ttu-id="92bdc-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="92bdc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bdc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bdc-118">-ResourceGroupName</span></span>
<span data-ttu-id="92bdc-119">Especifica o nome do grupo de recursos que contém a conta Batch.</span><span class="sxs-lookup"><span data-stu-id="92bdc-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="92bdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bdc-120">CommonParameters</span></span>
<span data-ttu-id="92bdc-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bdc-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92bdc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bdc-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92bdc-123">INPUTS</span></span>

### <span data-ttu-id="92bdc-124">System.String</span><span class="sxs-lookup"><span data-stu-id="92bdc-124">System.String</span></span>

## <span data-ttu-id="92bdc-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92bdc-125">OUTPUTS</span></span>

### <span data-ttu-id="92bdc-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="92bdc-126">System.Void</span></span>

## <span data-ttu-id="92bdc-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="92bdc-127">NOTES</span></span>

## <span data-ttu-id="92bdc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92bdc-128">RELATED LINKS</span></span>

[<span data-ttu-id="92bdc-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92bdc-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="92bdc-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92bdc-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="92bdc-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92bdc-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="92bdc-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92bdc-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="92bdc-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="92bdc-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="92bdc-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="92bdc-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


