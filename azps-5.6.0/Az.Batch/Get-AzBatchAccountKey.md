---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 07671d3318e599c9b63c4981df1ceac63178bb35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891887"
---
# <span data-ttu-id="1ad11-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ad11-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="1ad11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad11-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad11-103">Obtém as chaves de uma conta Batch.</span><span class="sxs-lookup"><span data-stu-id="1ad11-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="1ad11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ad11-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ad11-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ad11-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad11-106">O cmdlet **Get-AzBatchAccountKey** obtém as chaves de uma conta do Lote do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1ad11-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="1ad11-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ad11-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad11-108">Exemplo 1: Obter chaves de conta em lote e salvá-la em uma $Context para uso posterior</span><span class="sxs-lookup"><span data-stu-id="1ad11-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="1ad11-109">Este comando obtém os detalhes da conta e o armazena em um `$Context` objeto para uso posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1ad11-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="1ad11-110">Exemplo 2: Obter chaves de conta em lote e exibi-las</span><span class="sxs-lookup"><span data-stu-id="1ad11-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="1ad11-111">Este comando obtém as chaves da conta e as imprime no console.</span><span class="sxs-lookup"><span data-stu-id="1ad11-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="1ad11-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ad11-112">PARAMETERS</span></span>

### <span data-ttu-id="1ad11-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ad11-113">-AccountName</span></span>
<span data-ttu-id="1ad11-114">Especifica o nome da conta para a qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="1ad11-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="1ad11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad11-115">-DefaultProfile</span></span>
<span data-ttu-id="1ad11-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1ad11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ad11-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad11-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ad11-118">Especifica o nome do grupo de recursos que contém a conta para a qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="1ad11-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="1ad11-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad11-119">CommonParameters</span></span>
<span data-ttu-id="1ad11-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad11-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad11-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ad11-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad11-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ad11-122">INPUTS</span></span>

### <span data-ttu-id="1ad11-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1ad11-123">System.String</span></span>

## <span data-ttu-id="1ad11-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ad11-124">OUTPUTS</span></span>

### <span data-ttu-id="1ad11-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1ad11-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1ad11-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ad11-126">NOTES</span></span>

## <span data-ttu-id="1ad11-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ad11-127">RELATED LINKS</span></span>

[<span data-ttu-id="1ad11-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ad11-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="1ad11-129">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="1ad11-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
