---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601459"
---
# <span data-ttu-id="8d6e6-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d6e6-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="8d6e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6e6-103">Exclui um aplicativo de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="8d6e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d6e6-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d6e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d6e6-105">DESCRIPTION</span></span>
<span data-ttu-id="8d6e6-106">O cmdlet **Remove-AzBatchApplication** exclui um aplicativo de uma conta em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="8d6e6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d6e6-107">EXAMPLES</span></span>

### <span data-ttu-id="8d6e6-108">Exemplo 1: excluir um aplicativo de uma conta em lotes</span><span class="sxs-lookup"><span data-stu-id="8d6e6-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="8d6e6-109">Esse comando exclui o aplicativo Litware da conta ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="8d6e6-110">O comando falhará se o aplicativo contiver pacotes.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="8d6e6-111">OS</span><span class="sxs-lookup"><span data-stu-id="8d6e6-111">PARAMETERS</span></span>

### <span data-ttu-id="8d6e6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d6e6-112">-AccountName</span></span>
<span data-ttu-id="8d6e6-113">Especifica o nome da conta em lotes da qual esse cmdlet Remove um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="8d6e6-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8d6e6-114">-ApplicationId</span></span>
<span data-ttu-id="8d6e6-115">Especifica a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="8d6e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6e6-116">-DefaultProfile</span></span>
<span data-ttu-id="8d6e6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d6e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d6e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="8d6e6-119">Especifica o nome do grupo de recursos que contém a conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="8d6e6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6e6-120">CommonParameters</span></span>
<span data-ttu-id="8d6e6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d6e6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6e6-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6e6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6e6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d6e6-123">INPUTS</span></span>

### <span data-ttu-id="8d6e6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8d6e6-124">System.String</span></span>

## <span data-ttu-id="8d6e6-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d6e6-125">OUTPUTS</span></span>

### <span data-ttu-id="8d6e6-126">System. void</span><span class="sxs-lookup"><span data-stu-id="8d6e6-126">System.Void</span></span>

## <span data-ttu-id="8d6e6-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d6e6-127">NOTES</span></span>

## <span data-ttu-id="8d6e6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d6e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="8d6e6-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d6e6-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="8d6e6-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d6e6-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="8d6e6-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d6e6-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="8d6e6-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d6e6-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="8d6e6-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8d6e6-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="8d6e6-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8d6e6-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


