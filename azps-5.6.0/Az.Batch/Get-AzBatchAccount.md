---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 33ada04a3e45c1c8cc9768ef9da98abe781aa01a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886264"
---
# <span data-ttu-id="f59a2-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f59a2-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="f59a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f59a2-103">Obtém uma conta Batch na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f59a2-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="f59a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f59a2-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f59a2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f59a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f59a2-106">O cmdlet **Get-AzBatchAccount** obtém uma conta do Lote do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f59a2-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="f59a2-107">Você pode usar o *parâmetro AccountName* para obter uma única conta ou usar o *parâmetro ResourceGroupName* para obter contas nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f59a2-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="f59a2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f59a2-108">EXAMPLES</span></span>

### <span data-ttu-id="f59a2-109">Exemplo 1: Obter uma conta em lote pelo nome</span><span class="sxs-lookup"><span data-stu-id="f59a2-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="f59a2-110">Este comando obtém a conta em lote chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="f59a2-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="f59a2-111">Exemplo 2: Obter as contas em lotes associadas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f59a2-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="f59a2-112">Este comando obtém as contas em lotes associadas ao grupo de recursos CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="f59a2-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="f59a2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f59a2-113">PARAMETERS</span></span>

### <span data-ttu-id="f59a2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f59a2-114">-AccountName</span></span>
<span data-ttu-id="f59a2-115">Especifica o nome de uma conta.</span><span class="sxs-lookup"><span data-stu-id="f59a2-115">Specifies the name of an account.</span></span>
<span data-ttu-id="f59a2-116">Se você especificar um nome de conta, esse cmdlet retornará somente essa conta.</span><span class="sxs-lookup"><span data-stu-id="f59a2-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59a2-117">-DefaultProfile</span></span>
<span data-ttu-id="f59a2-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f59a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f59a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="f59a2-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f59a2-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f59a2-121">Se você especificar um grupo de recursos, esse cmdlet obtém as contas no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f59a2-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59a2-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="f59a2-122">-Tag</span></span>
<span data-ttu-id="f59a2-123">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f59a2-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f59a2-124">Por exemplo: @{key0="value0";key1=$null;key2="value2"} Este cmdlet obtém contas que contêm as marcas que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f59a2-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59a2-125">CommonParameters</span></span>
<span data-ttu-id="f59a2-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59a2-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59a2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59a2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f59a2-128">INPUTS</span></span>

### <span data-ttu-id="f59a2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f59a2-129">System.String</span></span>

### <span data-ttu-id="f59a2-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f59a2-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f59a2-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f59a2-131">OUTPUTS</span></span>

### <span data-ttu-id="f59a2-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f59a2-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f59a2-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="f59a2-133">NOTES</span></span>

## <span data-ttu-id="f59a2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f59a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="f59a2-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f59a2-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="f59a2-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f59a2-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="f59a2-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f59a2-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="f59a2-138">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="f59a2-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
