---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: ddc3bab48e766f80375fdf98add15e16e0086fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427301"
---
# <span data-ttu-id="65fb8-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fb8-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="65fb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="65fb8-103">Obtém uma conta em lotes na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="65fb8-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65fb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65fb8-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65fb8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="65fb8-106">O cmdlet **Get-AzureRmBatchAccount** Obtém uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="65fb8-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="65fb8-107">Você pode usar o parâmetro *AccountName* para obter uma única conta ou pode usar o parâmetro *ResourceGroupName* para obter contas sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65fb8-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="65fb8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65fb8-108">EXAMPLES</span></span>

### <span data-ttu-id="65fb8-109">Exemplo 1: obter uma conta em lotes por nome</span><span class="sxs-lookup"><span data-stu-id="65fb8-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="65fb8-110">Esse comando obtém a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="65fb8-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="65fb8-111">Exemplo 2: obter as contas em lotes associadas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="65fb8-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="65fb8-112">Esse comando obtém as contas em lotes associadas ao grupo de recursos CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="65fb8-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="65fb8-113">OS</span><span class="sxs-lookup"><span data-stu-id="65fb8-113">PARAMETERS</span></span>

### <span data-ttu-id="65fb8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65fb8-114">-AccountName</span></span>
<span data-ttu-id="65fb8-115">Especifica o nome de uma conta.</span><span class="sxs-lookup"><span data-stu-id="65fb8-115">Specifies the name of an account.</span></span>
<span data-ttu-id="65fb8-116">Se você especificar um nome de conta, esse cmdlet retornará apenas essa conta.</span><span class="sxs-lookup"><span data-stu-id="65fb8-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="65fb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fb8-117">-DefaultProfile</span></span>
<span data-ttu-id="65fb8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65fb8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fb8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fb8-119">-ResourceGroupName</span></span>
<span data-ttu-id="65fb8-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65fb8-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="65fb8-121">Se você especificar um grupo de recursos, esse cmdlet obterá as contas sob o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65fb8-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="65fb8-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="65fb8-122">-Tag</span></span>
<span data-ttu-id="65fb8-123">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="65fb8-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65fb8-124">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"} esse cmdlet obtém contas que contêm as marcas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="65fb8-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="65fb8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fb8-125">CommonParameters</span></span>
<span data-ttu-id="65fb8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fb8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fb8-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65fb8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fb8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65fb8-128">INPUTS</span></span>

### <span data-ttu-id="65fb8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="65fb8-129">System.String</span></span>

### <span data-ttu-id="65fb8-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65fb8-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="65fb8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65fb8-131">OUTPUTS</span></span>

### <span data-ttu-id="65fb8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="65fb8-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="65fb8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65fb8-133">NOTES</span></span>

## <span data-ttu-id="65fb8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65fb8-134">RELATED LINKS</span></span>

[<span data-ttu-id="65fb8-135">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fb8-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="65fb8-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fb8-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="65fb8-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fb8-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="65fb8-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="65fb8-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
