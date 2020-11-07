---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: a9289bc6a0db4403b96e982fd28f91578e3a0c9b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93785035"
---
# <span data-ttu-id="5f09b-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5f09b-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="5f09b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f09b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f09b-103">Obtém as chaves de uma conta em lotes.</span><span class="sxs-lookup"><span data-stu-id="5f09b-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="5f09b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f09b-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f09b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f09b-105">DESCRIPTION</span></span>
<span data-ttu-id="5f09b-106">O cmdlet **Get-AzBatchAccountKey** Obtém as chaves de uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5f09b-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="5f09b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f09b-107">EXAMPLES</span></span>

### <span data-ttu-id="5f09b-108">Exemplo 1: obter chaves da conta em lotes e salvá-la em $Context variável para uso posterior</span><span class="sxs-lookup"><span data-stu-id="5f09b-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="5f09b-109">Esse comando obtém os detalhes da conta e os armazena em um `$Context` objeto para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="5f09b-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="5f09b-110">Exemplo 2: obter chaves da conta em lotes e exibi-las</span><span class="sxs-lookup"><span data-stu-id="5f09b-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="5f09b-111">Esse comando obtém as chaves da conta e as imprime no console.</span><span class="sxs-lookup"><span data-stu-id="5f09b-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="5f09b-112">OS</span><span class="sxs-lookup"><span data-stu-id="5f09b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f09b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f09b-113">-AccountName</span></span>
<span data-ttu-id="5f09b-114">Especifica o nome da conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="5f09b-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f09b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f09b-115">-DefaultProfile</span></span>
<span data-ttu-id="5f09b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f09b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f09b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f09b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f09b-118">Especifica o nome do grupo de recursos que contém a conta para a qual esse cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="5f09b-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f09b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f09b-119">CommonParameters</span></span>
<span data-ttu-id="5f09b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f09b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f09b-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f09b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f09b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f09b-122">INPUTS</span></span>

### <span data-ttu-id="5f09b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5f09b-123">System.String</span></span>

## <span data-ttu-id="5f09b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f09b-124">OUTPUTS</span></span>

### <span data-ttu-id="5f09b-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5f09b-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5f09b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f09b-126">NOTES</span></span>

## <span data-ttu-id="5f09b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f09b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f09b-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5f09b-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="5f09b-129">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="5f09b-129">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


