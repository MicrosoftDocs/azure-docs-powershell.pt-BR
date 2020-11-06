---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427684"
---
# <span data-ttu-id="65fcf-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fcf-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="65fcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="65fcf-103">Obtém uma conta em lotes na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="65fcf-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65fcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65fcf-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65fcf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="65fcf-106">O cmdlet **Get-AzureRmBatchAccount** Obtém uma conta em lotes do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="65fcf-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="65fcf-107">Você pode usar o parâmetro *AccountName* para obter uma única conta ou pode usar o parâmetro *ResourceGroupName* para obter contas sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65fcf-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="65fcf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65fcf-108">EXAMPLES</span></span>

### <span data-ttu-id="65fcf-109">Exemplo 1: obter uma conta em lotes por nome</span><span class="sxs-lookup"><span data-stu-id="65fcf-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="65fcf-110">Esse comando obtém a conta em lotes chamada pfuller.</span><span class="sxs-lookup"><span data-stu-id="65fcf-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="65fcf-111">Exemplo 2: obter as contas em lotes associadas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="65fcf-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="65fcf-112">Esse comando obtém as contas em lotes associadas ao grupo de recursos CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="65fcf-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="65fcf-113">OS</span><span class="sxs-lookup"><span data-stu-id="65fcf-113">PARAMETERS</span></span>

### <span data-ttu-id="65fcf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65fcf-114">-AccountName</span></span>
<span data-ttu-id="65fcf-115">Especifica o nome de uma conta.</span><span class="sxs-lookup"><span data-stu-id="65fcf-115">Specifies the name of an account.</span></span>
<span data-ttu-id="65fcf-116">Se você especificar um nome de conta, esse cmdlet retornará apenas essa conta.</span><span class="sxs-lookup"><span data-stu-id="65fcf-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65fcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fcf-117">-DefaultProfile</span></span>
<span data-ttu-id="65fcf-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65fcf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fcf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65fcf-119">-ResourceGroupName</span></span>
<span data-ttu-id="65fcf-120">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65fcf-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="65fcf-121">Se você especificar um grupo de recursos, esse cmdlet obterá as contas sob o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65fcf-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65fcf-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="65fcf-122">-Tag</span></span>
<span data-ttu-id="65fcf-123">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="65fcf-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65fcf-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="65fcf-124">For example:</span></span>

<span data-ttu-id="65fcf-125">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="65fcf-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="65fcf-126">Esse cmdlet obtém contas que contêm as marcas que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="65fcf-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65fcf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fcf-127">CommonParameters</span></span>
<span data-ttu-id="65fcf-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fcf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fcf-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65fcf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fcf-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65fcf-130">INPUTS</span></span>

### <span data-ttu-id="65fcf-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65fcf-131">None</span></span>
<span data-ttu-id="65fcf-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="65fcf-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65fcf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65fcf-133">OUTPUTS</span></span>

### <span data-ttu-id="65fcf-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="65fcf-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="65fcf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65fcf-135">NOTES</span></span>

## <span data-ttu-id="65fcf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65fcf-136">RELATED LINKS</span></span>

[<span data-ttu-id="65fcf-137">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fcf-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="65fcf-138">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fcf-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="65fcf-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="65fcf-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="65fcf-140">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="65fcf-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)