---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 06d4632d9e7977639c708e81d4613b200189a2a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439967"
---
# <span data-ttu-id="c38df-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c38df-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="c38df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c38df-102">SYNOPSIS</span></span>
<span data-ttu-id="c38df-103">Obtém uma conta em lotes na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c38df-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c38df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c38df-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c38df-105">DESCRIPTION</span></span>
<span data-ttu-id="c38df-106">O cmdlet **Get-AzureRmBatchAccount** Obtém uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c38df-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="c38df-107">Você pode usar o parâmetro *AccountName* para obter uma única conta ou pode usar o parâmetro *ResourceGroupName* para obter contas sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c38df-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="c38df-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c38df-108">EXAMPLES</span></span>

### <span data-ttu-id="c38df-109">Exemplo 1: obter uma conta em lotes por nome</span><span class="sxs-lookup"><span data-stu-id="c38df-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="c38df-110">Esse comando obtém a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="c38df-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="c38df-111">Exemplo 2: obter as contas em lotes associadas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c38df-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="c38df-112">Esse comando obtém as contas em lotes associadas ao grupo de recursos CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="c38df-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="c38df-113">OS</span><span class="sxs-lookup"><span data-stu-id="c38df-113">PARAMETERS</span></span>

### <span data-ttu-id="c38df-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c38df-114">-AccountName</span></span>
<span data-ttu-id="c38df-115">Especifica o nome de uma conta.</span><span class="sxs-lookup"><span data-stu-id="c38df-115">Specifies the name of an account.</span></span>
<span data-ttu-id="c38df-116">Se você especificar um nome de conta, esse cmdlet retornará apenas essa conta.</span><span class="sxs-lookup"><span data-stu-id="c38df-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="c38df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38df-117">-ResourceGroupName</span></span>
<span data-ttu-id="c38df-118">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c38df-118">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c38df-119">Se você especificar um grupo de recursos, esse cmdlet obterá as contas sob o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c38df-119">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="c38df-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="c38df-120">-Tag</span></span>
<span data-ttu-id="c38df-121">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c38df-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c38df-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c38df-122">For example:</span></span>

<span data-ttu-id="c38df-123">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c38df-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="c38df-124">Esse cmdlet obtém contas que contêm as marcas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c38df-124">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="c38df-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38df-125">-DefaultProfile</span></span>
<span data-ttu-id="c38df-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c38df-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c38df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38df-127">CommonParameters</span></span>
<span data-ttu-id="c38df-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38df-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38df-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38df-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c38df-130">INPUTS</span></span>

## <span data-ttu-id="c38df-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c38df-131">OUTPUTS</span></span>

### <span data-ttu-id="c38df-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c38df-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c38df-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c38df-133">NOTES</span></span>

## <span data-ttu-id="c38df-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c38df-134">RELATED LINKS</span></span>

[<span data-ttu-id="c38df-135">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c38df-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="c38df-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c38df-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="c38df-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="c38df-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="c38df-138">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c38df-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
